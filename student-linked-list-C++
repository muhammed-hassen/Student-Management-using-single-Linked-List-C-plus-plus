#include<iostream>
using namespace std;
class node{
	public:
	string name;
	int age;
	string sex;
	node* next;
	
};
class student{
	private: node* head;
	public:
	 void view();
	 void search(string name);
	 void delt(string name);
	 void insert(string name,int age,string sex,int pos);
	 student()
	 {
	 	head=NULL;
	 }
	 bool isEmpty()
	 {
	 	if(head==NULL)
	 	{
	 		return true;
	 	}
	 	else
	 		return false;
	 }
	
};
void student::delt(string name)
{
	if(isEmpty())
	{
		cout<<"\nthere is no element in the list";
		
	}
	else
	{
		node* temp=head;
		node* back=NULL;
		while(temp && temp->name!=name)
		{
			back=temp;
			temp=temp->next;
			
		}
		if(temp)//the de;ete element is found
		{
			if(back==NULL)//if it is the first node
			{
				if(temp->next)///and it not the last elemnt in the lis
				{
					head=temp->next;
					delete temp;
					cout<<"\nsuccefuly deleted from the first place";
				}
				else{
					head=NULL;
					delete temp;
					cout<<"\nsucefully deleted ";
				}
				
			}
			else//there is previous node
			{
				if(temp->next)//if it is the middle element
				{
					back->next=temp->next;
					delete temp;
					cout<<"\nsucefuuly deleted from  them middle";
				}
				else
				{
					back=NULL;
					delete temp;
					cout<<"\nsucefullly deleted from the last element";
				}
				
			}
			
			
		}
		else
		{
			cout<<"\nthere is no such record with the requested name";
		}
	}
	
	
}
void student::search(string name)
{
	if(isEmpty())
	{
		cout<<"\nthe list is empty";
	}
	else
	{
		node* temp=head;
		while(temp && temp->name!=name)
		{
			temp=temp->next;
			
		}
		if(temp)
		{
			cout<<"\nNAME \t AGE \t SEX";
			cout<<"\n"<<temp->name<<"\t"<<temp->age<<"\t"<<temp->sex;
		}
		else{
			cout<<"\nthere is no such record found on the list";
		}
	}
}
void student::insert(string name,int age,string sex,int pos)
{
node*	newnode=new node();
		newnode->name=name;
		newnode->age=age;
		newnode->sex=sex;
		//case 1 on empty  list
	if(pos==0)
	{
		if(isEmpty())
		{
		
			head=newnode;
			cout<<"\nsuceffuly stored";
		}
		else{
			newnode->next=head;
			head=newnode;
			cout<<"\nsuceffuly stored";
		}
		
		
	}
	else if(pos>0)//case 2 if the list  is not empty
	{
		node* temp=head;
		cout<<pos;
		int i=1;
		
		while(temp && pos!=i)
		{
			temp=temp->next;
			i++;
			
		}
		if(temp)/// the postion is get
		{
			//case 1 if it is in midddle
			if(temp->next)
			{
				newnode->next=temp->next;
				temp->next=newnode;
				cout<<"\ninsert inthe middle ";
			}
			else//if it is in last
			{
				cout<<"\ninsert at last "<<temp->name;
				newnode->next=NULL;
				temp->next=newnode;
			
			}
			cout<<"\nsuceffuly stored";
			
		}
		else//the postion is not valid
		{
			cout<<"\nthere is no such place ";
			
		}
	}
	else
	{
		cout<<"\n invalid  postion requested";
	}

	
}
void student::view()
{
	if(!isEmpty())
	{
		node* temp=head;
		cout<<"\nName\t age \t sex";
		while(temp)
		{
			cout<<"\n"<<temp->name<<"\t"<<temp->age<<"\t"<<temp->sex;
			temp=temp->next;
			
		}
	}
}
int main()
{
	int choice;
	string name,sex;
	int age,pos;
	student su;
	do{
	
	cout<<"\n============ STUDENT MANAGMENT ========";
	cout<<"\n1.Insert";
	cout<<"\n2.view";
	cout<<"\n3.search";
	cout<<"\n4.delete";
	cout<<"\n5.exit";
	cin>>choice;
	switch(choice)
	{
		case 1:
			cout<<"\nEnter  name";
			cin>>name;
			cout<<"\nEnter age";
			cin>>age;
			cout<<"\nEnter sex";
			cin>>sex;
			cout<<"\nEnter the postion";
			cin>>pos;
			
			su.insert(name,age,sex,pos);
			break;
		case 2:
			su.view();
			break;
		case 3:
			cout<<"\nEnter the name ";
			cin>>name;
			su.search(name);
			break;
		case 4:
			cout<<"\nEnter the name to be deleted";
			cin>>name;
			su.delt(name);
			//getche();
			break;
			
		
		 
	}
	
	
}while(choice!=5);
	
}
