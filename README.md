import java.util.*;

class StuRecords{
static int [] roll_list={1001,1002,1003,1004};
static String [] names={"Amit","Ajay","Om","Kaya"};
static String [] branch_list={"CS","IT","CS","IT"};
}
class StuInfoSystem{
public static void main(String [] args){
String menu="press 1 for list all students\n";
menu = menu+"press 2 for search student\n\n";
menu = menu+"enter your choice:";
System.out.println(menu);
Scanner s=new Scanner(System.in);
int ch=Integer.parseInt(s.nextLine());
if(ch==1){
listAllStudent();
}
else if(ch==2){
System.out.print("Enter your roll no:");

int r = Integer.parseInt(s.nextLine());
findStudent(r);
}
else{
System.err.println("invalid choice\007");
}
}

static void listAllStudent(){
System.out.println("Student details:");
for(int i=0;i<StuRecords.roll_list.length;i++){
System.out.println("roll_no  "+StuRecords.roll_list[i]);
System.out.println("name  "+StuRecords.names[i]);
System.out.println("branch  "+StuRecords.branch_list[i]);
System.out.println("---------------------------");
}
}
static void findStudent(int rn){
boolean status = false;
for(int i=0;i<StuRecords.roll_list.length;i++){
if(StuRecords.roll_list[i]==rn){
status=true;
System.out.println("roll_no  "+StuRecords.roll_list[i]);
System.out.println("name  "+StuRecords.names[i]);
System.out.println("branch  "+StuRecords.branch_list[i]);
System.out.println("---------------------------");
}
}
if(status==false){
System.out.println("no record found");
}

}
}
