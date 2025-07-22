SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Admin(
	AdminId int NOT NULL,
	Admin_UserID int NOT NULL,
	Name varchar(30) NULL,
	Designation varchar(30) NULL,
	Email varchar(30) NULL,
	Contact varchar(30) NULL,
	Address varchar(30) NULL,
	CONSTRAINT [Pk_AdminId] PRIMARY KEY CLUSTERED 
(
	AdminId ASC
));


SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
 CREATE TABLE Admin_Login(
	AdminId int NOT NULL,
	Admin_UserID int NOT NULL,
	Password varchar(30) NULL,
PRIMARY KEY CLUSTERED 
(
	[Admin_UserID] ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Afsanay(
	CategoryId int NOT NULL,
	ISBN int NOT NULL ,
	Book_Name varchar(30) NULL,
	Author_Name varchar(30) NULL,
	Publisher_Name varchar(30) NULL,
	Language varchar(30) NULL,
	Price int NOT NULL
	 CONSTRAINT [Pk_ISBN18] PRIMARY KEY CLUSTERED 
(
	ISBN ASC
)
);

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE audio_book(
	isbn int NOT NULL,
	book_name varchar(50) NULL,
	author_id int NULL,
	author_name varchar(50) NULL,
	price int NULL,
	category_id int NULL,
	voice varchar(50) NULL,
 CONSTRAINT [PK_audio_book] PRIMARY KEY CLUSTERED 
(
	isbn ASC
));




SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Author(
	AuthorID int NOT NULL,
	Name varchar(50) NULL,
 CONSTRAINT [Pk_AuthorId] PRIMARY KEY CLUSTERED 
(
	AuthorID ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE bills_paid(
	bilL_id int NOT NULL,
	order_id int NULL,
	supplier_id int NULL,
	supplier_name varchar(50) NULL,
	amount_paid nchar(10) NULL,
	Date date NULL,
 CONSTRAINT [PK_bills_paid] PRIMARY KEY CLUSTERED 
(
	bilL_id ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Biography(
	Category_Id int NOT NULL,
	ISBN int NOT NULL,
	Book_Name varchar(30) NULL,
	Author_Name varchar(30) NULL,
	Publisher_Name varchar(30) NULL,
	Language varchar(30) NULL,
	Price int NOT NULL,
 CONSTRAINT [Pk_ISBN1] PRIMARY KEY CLUSTERED 
(
	ISBN ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE books(
	isbn int NOT NULL,
	book_name varchar(50) NOT NULL,
	category_id int NOT NULL,
	author_id int NOT NULL,
	author_name varchar(50) NOT NULL,
	publisher_id int NOT NULL,
	publisher_name varchar(50) NOT NULL,
	price int NULL,
 CONSTRAINT [PK_books] PRIMARY KEY CLUSTERED 
(
	isbn ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Business(
	Category_Id int NOT NULL,
	ISBN int NOT NULL,
	Book_Name varchar(30) NULL,
	Author_Name varchar(30) NULL,
	Publisher_Name varchar(30) NULL,
	Language varchar(30) NULL,
	Price int NOT NULL,
 CONSTRAINT [Pk_ISBN2] PRIMARY KEY CLUSTERED 
(
	ISBN ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Category(
	Category_Id int NOT NULL,
	Category_Name varchar(30) NULL,
 CONSTRAINT [Pk_Category_Id] PRIMARY KEY CLUSTERED 
(
	Category_Id ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Children(
	Category_Id int NOT NULL,
	ISBN int NOT NULL,
	Book_Name varchar(30) NULL,
	Author_Name varchar(30) NULL,
	Publisher_Name varchar(30) NULL,
	Language varchar(30) NULL,
	Price int NOT NULL,
 CONSTRAINT [Pk_ISBN3] PRIMARY KEY CLUSTERED 
(
	ISBN ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE Comics(
	Category_Id int NOT NULL,
	ISBN int NOT NULL,
	Book_Name varchar(30) NULL,
	Author_Name varchar(30) NULL,
	Publisher_Name varchar(30) NULL,
	Language varchar(30) NULL,
	Price int NOT NULL,
 CONSTRAINT [Pk_ISBN4] PRIMARY KEY CLUSTERED 
(
	ISBN ASC
));


SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Company(
	CompanyId int NOT NULL,
	Name varchar(30) NULL,
	Address varchar(30) NULL,
	Phone int NOT NULL,
	Website varchar(30) NULL,
	Email varchar(30) NULL,
 CONSTRAINT [Pk_CompanyId] PRIMARY KEY CLUSTERED 
(
	CompanyId ASC
));



SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE contact_staff(
	contact int NOT NULL,
	staff_id int NOT NULL,
	email varchar(50) NULL,
 CONSTRAINT [PK_contact_staff] PRIMARY KEY CLUSTERED 
(
	contact ASC
));


SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE [dbo].[contacts_clients](
	[contact] [int] NOT NULL,
	[client_id] [int] NOT NULL,
	[email] [varchar](50) NULL,
 CONSTRAINT [PK_contacts_clients] PRIMARY KEY CLUSTERED 
(
	[contact] ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Cook_Books(
	Category_Id int NOT NULL,
	ISBN int NOT NULL,
	Book_Name varchar(30) NULL,
	Author_Name varchar(30) NULL,
	Publisher_Name varchar(30) NULL,
	Language varchar(30) NULL,
	Price int NOT NULL,
 CONSTRAINT [Pk_ISBN5] PRIMARY KEY CLUSTERED 
(
	ISBN ASC
));


SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Customer_Service(
	ComplainNo int NOT NULL,
	TrackingId int NOT NULL,
	Email varchar(30) NULL,
	Query varchar(50) NULL,
	Query_Date date NULL,
	Status varchar(30) NULL,
 CONSTRAINT [Pk_Ids] PRIMARY KEY CLUSTERED 
(
	ComplainNo ASC,
	TrackingId ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Department(
	DeptId int NOT NULL,
	DeptName varchar(20) NULL,
	Working_Hours time(7) NULL,
PRIMARY KEY CLUSTERED 
(
	DeptId ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Events(
	EventId int NOT NULL,
	Event_Name varchar(20) NULL,
	Event_date date NULL,
	Event_time time(7) NULL,
	Product varchar(30) NULL,
	AuthorID int NOT NULL,
	AuthorName varchar(30) NULL,
 CONSTRAINT [Pk_EventId] PRIMARY KEY CLUSTERED 
(
	EventId ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Fantasy(
	Category_Id int NOT NULL,
	ISBN int NOT NULL,
	Book_Name varchar(30) NULL,
	Author_Name varchar(30) NULL,
	Publisher_Name varchar(30) NULL,
	Language varchar(30) NULL,
	Price int NOT NULL,
 CONSTRAINT [Pk_ISBN6] PRIMARY KEY CLUSTERED 
(
	ISBN ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Fiction(
	Category_Id int NOT NULL,
	ISBN int NOT NULL,
	Book_Name varchar(30) NULL,
	Author_Name varchar(30) NULL,
	Publisher_Name varchar(30) NULL,
	Language varchar(30) NULL,
	Price int NOT NULL,
 CONSTRAINT [Pk_ISBN14] PRIMARY KEY CLUSTERED 
(
	ISBN ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE History(
	Category_Id int NOT NULL,
	ISBN int NOT NULL,
	Book_Name varchar(30) NULL,
	Author_Name varchar(30) NULL,
	Publisher_Name varchar(30) NULL,
	Language varchar(30) NULL,
	Price int NOT NULL,
 CONSTRAINT [Pk_ISBN7] PRIMARY KEY CLUSTERED 
(
	ISBN ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Horror(
	Category_Id int NOT NULL,
	ISBN int NOT NULL,
	Book_Name varchar(30) NULL,
	Author_Name varchar(30) NULL,
	Publisher_Name varchar(30) NULL,
	Language varchar(30) NULL,
	Price int NOT NULL,
 CONSTRAINT [Pk_ISBN8] PRIMARY KEY CLUSTERED 
(
	ISBN ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Humor(
	Category_Id int NOT NULL,
	ISBN int NOT NULL,
	Book_Name varchar(30) NULL,
	Author_Name varchar(30) NULL,
	Publisher_Name varchar(30) NULL,
	Language varchar(30) NULL,
	Price int NOT NULL,
 CONSTRAINT [Pk_ISBN9] PRIMARY KEY CLUSTERED 
(
	ISBN ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE item_category(
	item_c_id int NOT NULL,
	cateory_name varchar(50) NULL,
 CONSTRAINT [PK_item_category] PRIMARY KEY CLUSTERED 
(
	item_c_id ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Items(
	item_id int NOT NULL,
	name varchar(50) NULL,
	item_category int NULL,
	price int NULL,
	whole_seller_id int NULL,
	company_id int NULL,
 CONSTRAINT [PK_Items] PRIMARY KEY CLUSTERED 
(
	item_id ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE member_info(
	client_id int NOT NULL,
	name varchar(50) NOT NULL,
	contact int NULL,
	address varchar(50) NOT NULL,
	membership_id int NULL,
 CONSTRAINT [PK_members] PRIMARY KEY CLUSTERED 
(
	client_id ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE members(
	membership_id int NOT NULL,
	client_id int NOT NULL,
	name varchar(50) NULL,
	date_of_membership date NULL,
	expriy_of_membership date NULL,
 CONSTRAINT [PK_members_1] PRIMARY KEY CLUSTERED 
(
	membership_id ASC
));

CREATE TABLE Movie(
	DvdId int NOT NULL,
	Title varchar(30) NULL,
	Genre varchar(30) NULL,
	Release_Date date NULL,
	Producer varchar(30) NULL,
	Format varchar(30) NULL,
	For_delivery varchar(30) NULL,
	Price int NOT NULL,
 CONSTRAINT [Pk_DvdId] PRIMARY KEY CLUSTERED 
(
	DvdId ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Mystery(
	Category_Id int NOT NULL,
	ISBN int NOT NULL,
	Book_Name varchar(30) NULL,
	Author_Name varchar(30) NULL,
	Publisher_Name varchar(30) NULL,
	Language varchar(30) NULL,
	Price int NOT NULL,
 CONSTRAINT [Pk_ISBN10] PRIMARY KEY CLUSTERED 
(
	ISBN ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE order_generated(
	order_id int NOT NULL,
	supplier_id int NOT NULL,
	amount int NOT NULL,
	quantity_of_items int NULL,
	date date NULL,
 CONSTRAINT [PK_order_generated] PRIMARY KEY CLUSTERED 
(
	order_id ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE orders(
	order_id int NOT NULL,
	client_id int NOT NULL,
	item_id int NULL,
	item_name varchar(50) NULL,
	isbn int NULL,
	book_name varchar(50) NULL,
	total_bill int NOT NULL,
	date date NOT NULL,
 CONSTRAINT [PK_orders] PRIMARY KEY CLUSTERED 
(
	order_id ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Poetry(
	Category_Id int NOT NULL,
	ISBN int NOT NULL,
	Book_Name varchar(30) NULL,
	Author_Name varchar(30) NULL,
	Publisher_Name varchar(30) NULL,
	Language varchar(30) NULL,
	Price int NOT NULL,
 CONSTRAINT [Pk_ISBN16] PRIMARY KEY CLUSTERED 
(
	ISBN ASC
));


SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Promotions(
	PromoId int NOT NULL,
	Promo_Name varchar(30) NULL,
	ISBN int NOT NULL,
	Book_Name varchar(30) NULL,
	Original_Price int NOT NULL,
	Discounted_Price int NOT NULL,
	Gift varchar(30) NULL,
 CONSTRAINT [Pk_PromoId] PRIMARY KEY CLUSTERED 
(
	PromoId ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Publisher(
	PublisherID int NOT NULL,
	Name varchar(50) NULL,
 CONSTRAINT [Pk_PublisherId] PRIMARY KEY CLUSTERED 
(
	PublisherID ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Query(
	QueryId int NOT NULL,
	Name varchar(30) NULL,
	Email varchar(30) NULL,
	Date_of_Query date NULL,
 CONSTRAINT [Pk_QueryId] PRIMARY KEY CLUSTERED 
(
	QueryId ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE recipt(
	recipt_id int NOT NULL,
	client_id int NULL,
	membership_id int NULL,
	amount_charge int NULL,
	date date NULL,
 CONSTRAINT [PK_recipt] PRIMARY KEY CLUSTERED 
(
	recipt_id ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Romance(
	CategoryId int NOT NULL,
	ISBN int NOT NULL,
	Book_Name varchar(30) NULL,
	Author_Name varchar(30) NULL,
	Publisher_Name varchar(30) NULL,
	Language varchar(30) NULL,
	Price int NOT NULL,
 CONSTRAINT [Pk_ISBN13] PRIMARY KEY CLUSTERED 
(
	ISBN ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Sci_Fi(
	Category_Id int NOT NULL,
	ISBN int NOT NULL,
	Book_Name varchar(30) NULL,
	Author_Name varchar(30) NULL,
	Publisher_Name varchar(30) NULL,
	Language varchar(30) NULL,
	Price int NOT NULL,
 CONSTRAINT [Pk_ISBN17] PRIMARY KEY CLUSTERED 
(
	ISBN ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Science(
	Category_Id int NOT NULL,
	ISBN int NOT NULL,
	Book_Name varchar(30) NULL,
	Author_Name varchar(30) NULL,
	Publisher_Name varchar(30) NULL,
	Language varchar(30) NULL,
	Price int NOT NULL,
 CONSTRAINT [Pk_ISBN11] PRIMARY KEY CLUSTERED 
(
	ISBN ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Self_Help(
	[CategoryId] [int] NOT NULL,
	ISBN int NOT NULL,
	Book_Name varchar(30) NULL,
	Author_Name varchar(30) NULL,
	Publisher_Name varchar(30) NULL,
	Language varchar(30) NULL,
	Price int NOT NULL,
 CONSTRAINT [Pk_ISBN12] PRIMARY KEY CLUSTERED 
(
	ISBN ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE SoldBooks(
	ISBN int NOT NULL,
	Book_Name varchar(30) NULL,
	Date date NULL,
	Price int NOT NULL,
 );

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Staff(
	StaffID int NOT NULL,
	Name varchar(30) NULL,
	DateOfJoining int NULL,
	Salary int NULL,
	Address varchar(30) NULL,
	DeparmentID int NOT NULL,
	DepartmentName varchar(30) NULL,
 CONSTRAINT [Pk_StaffId] PRIMARY KEY CLUSTERED 
(
	StaffID ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Supplier(
	SupplierId int NOT NULL,
	Name varchar(30) NULL,
	Address varchar(30) NULL,
	Phone int NOT NULL,
	Email varchar(30) NULL,
 CONSTRAINT [Pk_SupplierId] PRIMARY KEY CLUSTERED 
(
	SupplierId ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE Crime(
	Category_Id int NOT NULL,
	ISBN int NOT NULL,
	Book_Name varchar(30) NULL,
	Author_Name varchar(30) NULL,
	Publisher_Name varchar(30) NULL,
	Language varchar(30) NULL,
	Price int NOT NULL,
 CONSTRAINT [Pk_ISBN15] PRIMARY KEY CLUSTERED 
(
	ISBN ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE walk_incustomer(
	client_id int NOT NULL,
	name varchar(50) NULL,
	contact varchar(50) NULL,
	email varchar(50) NULL,
 CONSTRAINT [PK_walk_incustomer] PRIMARY KEY CLUSTERED 
(
	client_id ASC
));

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE WholeSeller(
	WholeSellerId int NOT NULL,
	Name varchar(30) NULL,
	Address varchar(30) NULL,
Phone int NOT NULL,
	Email varchar(30) NULL,
 CONSTRAINT [Pk_WSID] PRIMARY KEY CLUSTERED 
(
	WholeSellerId ASC
));


INSERT Admin_Login (AdminId, Admin_UserID, Password) 
VALUES 
(1, 1001, N'shaheer123')
INSERT Admin_Login (AdminId, Admin_UserID, Password)
 VALUES 
 (2, 1002, N'ahmed237')
INSERT Admin_Login (AdminId, Admin_UserID, Password)
 VALUES
  (3, 1003, N'aun523')
INSERT Admin_Login (AdminId, Admin_UserID, Password)
 VALUES
  (4, 1004, N'sadiq123')


INSERT Admin (AdminId, Admin_UserID, Name, Designation, Email, Contact, Address) 
VALUES
 (1, 1001, N'shaheer', N'Head', N'shaheer99@gmail.com', N'03002134654', N'h-89 sector11s state LA usa')
INSERT Admin (AdminId, Admin_UserID, Name, Designation, Email, Contact, Address) 
VALUES
 (2, 1002, N'ahmed', N'deputy-head', N'ahmed19@gmail.com', N'03002134654', N'h-89 sector11s state LA usa')
INSERT Admin (AdminId, Admin_UserID, Name, Designation, Email, Contact, Address)
 VALUES
  (3, 1003, N'aun', N'director', N'aun189@gmail.com', N'03002134654', N'h-100 shantinagar paglapur')
INSERT Admin (AdminId, Admin_UserID, Name, Designation, Email, Contact, Address) 
VALUES
 (4, 1003, N'sadiq', N'deputy-director', N'sadiq9@gmail.com', N'03002134654', N'h-100 los angles')


INSERT Afsanay (CategoryId, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price)
 VALUES
  (18, 979969021, N'Bang E Dara', N'Allama Muhammad Iqbal', N'Ferozsons (Private) Limited', N'Urdu', 6700)
INSERT Afsanay (CategoryId, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) 
VALUES
 (18, 979969029, N'Zarbe Kaleem', N'Allama Muhammad Iqbal', N'Ferozsons (Private) Limited', N'Urdu', 7505)
INSERT Afsanay (CategoryId, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) 
VALUES
 (18, 1000007641, N'Aur Kuch Khowab', N'Ushna Kausar Sardar', N'Ilmoirfan Publishers', N'Urdu', 670)
INSERT Afsanay (CategoryId, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price)
 VALUES
  (18, 1000007646, N'Mohabbat Rabt Hay', N'Ushna Kausar Sardar', N'Ilmoirfan Publishers', N'Urdu', 750)
INSERT Afsanay (CategoryId, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) 
VALUES
 (18, 1000007649, N'Band Gali', N'Ushna Kausar Sardar', N'Ilmoirfan Publishers', N'Urdu', 900)


INSERT audio_book (isbn, book_name, author_id, author_name, price, category_id, voice) 
VALUES
 (1936321, N'selp-help manual', 1034, N'gerald alper', 1200, 19, N'colin')
INSERT audio_book (isbn, book_name, author_id, author_name, price, category_id, voice) 
VALUES
 (1936322, N'selp-help manual', 1034, N'gerald alper', 5999, 19, N'colin')
INSERT audio_book (isbn, book_name, author_id, author_name, price, category_id, voice) 
VALUES
 (97815098, N'the wich', 1027, N'judy blume', 2050, 19, N'abhram')
INSERT audio_book (isbn, book_name, author_id, author_name, price, category_id, voice) 
VALUES
 (97969461, N'Mel meli dhoop', 1043, N'anwar maqsood', 4999, 19, N'hashim')
INSERT audio_book (isbn, book_name, author_id, author_name, price, category_id, voice) 
VALUES 
(399592520, N'dare to lead', 1006, N'brene brown', 4999, 19, N'colin')
INSERT audio_book (isbn, book_name, author_id, author_name, price, category_id, voice)
 VALUES
  (425235229, N'a killer pot', 1029, N'ellery adams', 7200, 19, N'colin')



INSERT Author (AuthorID, Name)
 VALUES 
 (1001, N'Walter Isaacson')
INSERT Author (AuthorID, Name)
 VALUES
  (1002, N'Bear Grylls')
INSERT Author (AuthorID, Name)
 VALUES
  (1003, N'Tom Felton')
INSERT Author (AuthorID, Name)
 VALUES
  (1004, N'Shibli Nomani')
INSERT Author (AuthorID, Name) 
VALUES
 (1005, N'Abdus Sattar Edhi')
INSERT Author (AuthorID, Name)
 VALUES
  (1006, N'Brené Brownr')
INSERT Author (AuthorID, Name)
 VALUES
  (1007, N'Chris Hogan')
INSERT Author (AuthorID, Name)
 VALUES
  (1008, N'Ian Siegel')
INSERT Author (AuthorID, Name)
 VALUES
  (1009, N'Simon Sinek')
INSERT Author (AuthorID, Name)
 VALUES
  (1010, N'Raja Rajamannar')
INSERT Author (AuthorID, Name) 
VALUES
 (1011, N'Ahmed Ali')
INSERT Author (AuthorID, Name)
 VALUES
  (1012, N'Margaret Wise')
INSERT Author (AuthorID, Name)
VALUES
 (1013, N'Antoine de Saint')
INSERT Author (AuthorID, Name) 
VALUES 
(1014, N'Kishwar Naheed')
INSERT Author (AuthorID, Name)
 VALUES
  (1015, N'Julia Donaldson')
INSERT Author (AuthorID, Name)
 VALUES
  (1016, N'Marvel Comics')
INSERT Author (AuthorID, Name)
 VALUES
  (1017, N'Archie Superstars')
INSERT Author (AuthorID, Name) 
VALUES
 (1018, N'J Kenji Lopz')
INSERT Author (AuthorID, Name)
 VALUES
  (1019, N'Gordon Ramsay')
INSERT Author (AuthorID, Name)
 VALUES 
 (1020, N'Robert Jordan')
INSERT Author (AuthorID, Name) 
VALUES
 (1021, N'Campbell Books')
INSERT Author (AuthorID, Name)
 VALUES
  (1022, N'Joseph Pfeifer')
INSERT Author (AuthorID, Name)
 VALUES
  (1023, N'Douglas Preston')
INSERT Author (AuthorID, Name)
 VALUES
  (1024, N'Craig Whitlock')
INSERT Author (AuthorID, Name) VALUES (1025, N'Stephen King')
INSERT Author (AuthorID, Name) VALUES (1026, N'Darcy Coates')
INSERT Author (AuthorID, Name) VALUES (1027, N'Judy Blume')
INSERT Author (AuthorID, Name) VALUES (1028, N'David Walliams')
INSERT Author (AuthorID, Name) VALUES (1029, N'Ellery Adams')
INSERT Author (AuthorID, Name) VALUES (1030, N'Tanya Huff')






INSERT bills_paid (bilL_id, order_id, supplier_id, supplier_name, amount_paid, date)
 VALUES
  (4001, 9903, 2101, N'aliza', N'1000.00   ', CAST(N'2017-09-12' AS Date))
INSERT bills_paid (bilL_id, order_id, supplier_id, supplier_name, amount_paid, date)
 VALUES 
 (4002, 9902, 2102, N'areeba', N'1000.00   ', CAST(N'2012-09-12' AS Date))


INSERT Biography (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (1, 907432643, N'Einstein His Life', N'Walter Isaacson', N'Simon & Schuster', N'English', 5600)
INSERT Biography (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (1, 1426222629, N'My Life in the Wild', N'Bear Grylls', N'National Geographic Society', N'English', 5700)
INSERT Biography (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (1, 1538741369, N'Beyond the Wand', N'Tom Felton', N'Grand Central Publishing', N'English', 4750)
INSERT Biography (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (1, 1538741520, N'Seerat-Un-Nabi', N'Shibli Nomani', N'Darul Musannefin Shibli', N'Urdu', 6070)
INSERT Biography (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (1, 1738761520, N'A Mirror to the Blind', N'Abdus Sattar Edhi', N'NationalBureau of Publications', N'Urdu', 2890)



INSERT books (isbn, book_name, category_id, author_id, author_name, publisher_id, publisher_name, price) VALUES (393081087, N'The Food Lab', 5, 1018, N'J Kenji Lopz', 2018, N'Norton & Company', 7000)
INSERT books (isbn, book_name, category_id, author_id, author_name, publisher_id, publisher_name, price) VALUES (393541215, N'The Wok', 5, 1018, N'J Kenji Lopz', 2018, N'Norton & Company', 5000)
INSERT books (isbn, book_name, category_id, author_id, author_name, publisher_id, publisher_name, price) VALUES (399592520, N'Dare to lead', 2, 1006, N'Brené Brownr', 2006, N'Random House', 5632)
INSERT books (isbn, book_name, category_id, author_id, author_name, publisher_id, publisher_name, price) VALUES (425235229, N'A Killer Plot', 10, 1029, N'Ellery Adams', 2019, N'Berkley Books', 590)
INSERT books (isbn, book_name, category_id, author_id, author_name, publisher_id, publisher_name, price) VALUES (425245004, N'The Last Word', 10, 1029, N'Ellery Adams', 2019, N'Berkley Books', 3450)
INSERT books (isbn, book_name, category_id, author_id, author_name, publisher_id, publisher_name, price) VALUES (425270831, N'Lethal Letters', 10, 1029, N'Ellery Adams', 2019, N'Berkley Books', 690)
INSERT books (isbn, book_name, category_id, author_id, author_name, publisher_id, publisher_name, price) VALUES (97815098, N'The Witch Kind', 9, 1027, N'Judy Blume', 2015, N'Macmillan', 890)
INSERT books (isbn, book_name, category_id, author_id, author_name, publisher_id, publisher_name, price) VALUES (97969461, N'MELI MELI DHOOP', 16, 1043, N'Anwar Masood', 2029, N'Book Corner', 220)
INSERT books (isbn, book_name, category_id, author_id, author_name, publisher_id, publisher_name, price) VALUES (316419486, N'The Witch Kind', 15, 1040, N'Louisa Morgan', 2026, N'Redhook', 6777)
INSERT books (isbn, book_name, category_id, author_id, author_name, publisher_id, publisher_name, price) VALUES (316508586, N'A Secret History of Witches', 15, 1040, N'Louisa Morgan', 2026, N'Redhook', 3450)


INSERT Business (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (2, 399592520, N'Dare to lead', N'Brené Brownr', N'Random House', N'English', 5632)
INSERT Business (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (2, 977489523, N'Everyday Millionaires', N'Chris Hogan', N'Ramsey Press', N'English', 2000)
INSERT Business (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (2, 1338761529, N'Get Hired Now!', N'Ian Siegel', N'Wiley', N'English', 2067)
INSERT Business (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (2, 1591848016, N'Leaders Eat Last ', N'Simon Sinek', N'Portfolio', N'English', 1299)
INSERT Business (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (2, 1738761529, N'Quantum Marketing', N'Raja Rajamannar', N'HarperCollins Leadership', N'English', 2000)



INSERT Category (Category_Id, Category_Name) VALUES (1, N'Biography')
INSERT Category (Category_Id, Category_Name) VALUES (2, N'Business')
INSERT Category (Category_Id, Category_Name) VALUES (3, N'Children')
INSERT Category (Category_Id, Category_Name) VALUES (4, N'Comics')
INSERT Category (Category_Id, Category_Name) VALUES (5, N'Cook books')
INSERT Category (Category_Id, Category_Name) VALUES (6, N'Fantasy')
INSERT Category (Category_Id, Category_Name) VALUES (7, N'History')
INSERT Category (Category_Id, Category_Name) VALUES (8, N'Horror')
INSERT Category (Category_Id, Category_Name) VALUES (9, N'Humor')
INSERT Category (Category_Id, Category_Name) VALUES (10, N'Mystery')
INSERT Category (Category_Id, Category_Name) VALUES (11, N'Science')
INSERT Category (Category_Id, Category_Name) VALUES (12, N'Self help')
INSERT Category (Category_Id, Category_Name) VALUES (13, N'Romance')
INSERT Category (Category_Id, Category_Name) VALUES (14, N'Gothic fiction')
INSERT Category (Category_Id, Category_Name) VALUES (15, N'True crime')
INSERT Category (Category_Id, Category_Name) VALUES (16, N'Poetry')
INSERT Category (Category_Id, Category_Name) VALUES (17, N'Sci fi') 
INSERT Category (Category_Id, Category_Name) VALUES (18, N'Afsanay')
INSERT Category (Category_Id, Category_Name) VALUES (19, N'audio books')


INSERT Children (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (3, 978000735, N'Sara Ki Billi', N'Ahmed Ali', N'Oxford', N'Urdu', 5200)
INSERT Children (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (3, 978024144, N'Good Night Moon', N'Margaret Wise', N'Harpor Brothers', N'English', 200)
INSERT Children (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (3, 978178504, N'The Little Prince', N'Antoine de Saint', N'Arbor Publishing', N'English', 1600)
INSERT Children (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (3, 978186197, N'Ghaas ki Guria', N'Kishwar Naheed', N'Sang e Meel', N'Urdu', 1500)
INSERT Children (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (3, 978817898, N'Grufallo the bear', N'Julia Donaldson', N'Macmillan', N'English', 980)





INSERT Comics (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (4, 978078512, N'Ghost Rider', N'Marvel Comics', N'Hachette Book Group', N'English', 1825)
INSERT Comics (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (4, 978164501, N'Archie: Modern Classics Magic', N'Archie Superstars', N'Penguin USA', N'English', 1895)
INSERT Comics (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (4, 978164576, N'Archie', N'Archie Superstars', N'Penguin USA', N'English', 2590)
INSERT Comics (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (4, 978164595, N'Black Widow', N'Marvel Comics', N'Hachette Book Group', N'English', 980)
INSERT Comics (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (4, 979868158, N'Spider-Man: Homecoming', N'Marvel Comics', N'Hachette Book Group', N'English', 1920)



INSERT Company (CompanyId, Name, Address, Phone, Website, Email) VALUES (2101, N'nexis', N'h-4 sector 4 b state vas', 300210303, N'www.nexis.com', N'nexis@gmail.com')
INSERT Company (CompanyId, Name, Address, Phone, Website, Email) VALUES (2102, N'narcos', N'h-4 sector 4 b state vas', 30021253, N'www.narcos.com', N'narcors@gmail.com')
INSERT Company (CompanyId, Name, Address, Phone, Website, Email) VALUES (2103, N'lexus', N'h-4 sector 4 b state vas', 30021253, N'www.lexus.com', N'lexus@gmail.com')
INSERT Company (CompanyId, Name, Address, Phone, Website, Email) VALUES (2104, N'dealing', N'h-4 sector 4 b state vas', 321021253, N'www.dealing.com', N'dealing@gmail.com')

INSERT contact_staff (contact, staff_id, email) VALUES (3021346, 12001, N'aslam12@gmail.com')
INSERT contact_staff (contact, staff_id, email) VALUES (3022134, 12003, N'neen12@gmail.com')
INSERT contact_staff (contact, staff_id, email) VALUES (30215465, 12002, N'don12@gmail.com')


INSERT Cook_Books (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (5, 393081087, N'The Food Lab', N'J Kenji Lopz', N'Norton & Company', N'English', 7000)
INSERT Cook_Books (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (5, 393541215, N'The Wok', N'J Kenji Lopz', N'Norton & Company', N'English', 5000)
INSERT Cook_Books (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (5, 1455525251, N'Home Cooking', N'Gordon Ramsay', N'Grand Central Publishing', N'English', 9000)
INSERT Cook_Books (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (5, 1538707810, N'Ramsay in 10', N'Gordon Ramsay', N'Grand Central Publishing', N'English', 9000)
INSERT Cook_Books (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (5, 1538719339, N'Quick and Delicious', N'Gordon Ramsay', N'Grand Central Publishing', N'English', 10000)






INSERT Department (DeptId, DeptName, Working_Hours) VALUES (3001, N'sales', CAST(N'08:00:00' AS Time))
INSERT Department (DeptId, DeptName, Working_Hours) VALUES (3002, N'marketing', CAST(N'09:00:00' AS Time))
INSERT Department (DeptId, DeptName, Working_Hours) VALUES (3003, N'store-keeping', CAST(N'09:00:00' AS Time))


INSERT Events (EventId, Event_Name, Event_date, Event_time, Product, AuthorID, AuthorName) VALUES (12001, N'inspiring youngsters', CAST(N'2022-06-02' AS Date), CAST(N'09:00:00' AS Time), N'book', 1001, N'walter isaacson')
INSERT Events (EventId, Event_Name, Event_date, Event_time, Product, AuthorID, AuthorName) VALUES (12002, N'mind booster', CAST(N'2012-06-02' AS Date), CAST(N'12:00:00' AS Time), N'book', 1009, N'simson')
INSERT Events (EventId, Event_Name, Event_date, Event_time, Product, AuthorID, AuthorName) VALUES (12003, N'booster', CAST(N'2013-06-02' AS Date), CAST(N'01:00:00' AS Time), N'book', 1013, N'antoine')


INSERT Fantasy(Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (6, 978356503, N'Knife Of Dreams', N'Robert Jordan', N'Simon & Schuster', N'English', 395)
INSERT Fantasy (Category_Id,ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (6, 978356504, N'The Path Of Daggers', N'Robert Jordan', N'Simon & Schuster', N'English', 980)
INSERT Fantasy (Category_Id, ISBN,Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (6, 978529003, N'Aladdin', N'Campbell Books', N'Macmillian', N'English', 898)
INSERT Fantasy (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (6, 978529004, N'Beautiful Birds', N'Campbell Books', N'Macmillian', N'English', 700)
INSERT Fantasy (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (6, 978529005, N'Goth Girl', N'Campbell Books', N'Macmillian', N'English', 828)


INSERT Fiction (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (14, 1813326, N'Dracula', N'Bram Stoker', N'Avon Books', N'English', 898)
INSERT Fiction (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (14, 1813626, N'Frankenstein', N'Bram Stoker', N'Avon Books', N'English', 700)
INSERT Fiction (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (14, 1813926, N'Strange Case', N'Bram Stoker', N'Avon Books', N'English', 828)


INSERT History (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (7, 593330250, N'Ordinary Heroes', N'Joseph Pfeifer', N'Portfolio', N'English', 5000)
INSERT History (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (7, 1426221983, N'Lost Cities, Ancient Tombs', N'Douglas Preston', N'National Geographic Society', N'English', 5800)
INSERT History (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name,Language, Price) VALUES (7, 1982159006, N'The Afghanistan Papers', N'Craig Whitlock', N'Simon & Schuster', N'English', 4670)



INSERT Horror (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (8, 1501143107, N'Misery', N'Stephen King', N'Berkley Books', N'English', 790)
INSERT Horror (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (8, 1501182099, N'IT', N'Stephen King', N'Scribner Book Company', N'English', 6000)
INSERT Horror (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (8, 1728220173, N'Hunted', N'Darcy Coates', N'Poisoned Pen Press', N'English', 5799)
INSERT Horror (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (8, 1728221773, N'Dead Lake', N'Darcy Coates', N'Poisoned Pen Press', N'English', 2350)
INSERT Horror (Category_Id,ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (8, 1982148241, N'The Outsider', N'Stephen King', N'Gallery Books', N'English', 450)


INSERT Humor (Category_Id, ISBN, Book_Name, Author_Name,Publisher_Name, Language, Price) VALUES (9, 97815098, N'The Witch Kind', N'Judy Blume', N'Macmillan', N'English', 890)
INSERT Humor (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (9, 978000727, N'Mr Stink', N'David Walliams', N'Harper Collins UK', N'English', 4500)
INSERT Humor (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (9, 978000737, N'Billionaire Boy', N'David Walliams', N'Harper Collins UK', N'English', 2300)
INSERT Humor (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (9, 978000745, N'Awful Auntie', N'David Walliams', N'Harper Collins UK', N'English', 2100)
INSERT Humor (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (9, 978144726, N'Double Fudge', N'Judy Blume', N'Macmillan', N'English', 1200)


INSERT Items (item_id, name, item_category, price, whole_seller_id, company_id) VALUES (10011, N'abc-journal', 1, 89, 3001, 2101)
INSERT Items (item_id, name, item_category, price, whole_seller_id, company_id) VALUES (10012, N'Pakistan-map', 2, 190, 3001, 2103)
INSERT Items (item_id, name, item_category, price, whole_seller_id, company_id) VALUES (10013, N'spiral-journal', 1, 190, 3001, 2101)



INSERT item_category (item_c_id, cateory_name) VALUES (1, N'journals')
INSERT item_category (item_c_id, cateory_name) VALUES (2, N'maps')
INSERT item_category (item_c_id, cateory_name) VALUES (3, N'boomarks')



INSERT member_info (client_id, name, contact, address, membership_id) VALUES (5005, N'ahmed', 2015001, N'h-4 sector 11-a state LA', 2015001)
INSERT member_info (client_id, name, contact, address, membership_id) VALUES (5006, N'akbar', 2015002, N'h-4 sector 11-a state LA', 2015002)
INSERT member_info (client_id, name, contact, address, membership_id) VALUES (5007, N'alina', 2015003, N'h-4 sector 11-a state LA', 2015003)


INSERT members (membership_id, client_id, name, date_of_membership, expriy_of_membership) VALUES (2015001, 5005, N'ahmed', CAST(N'2015-08-09' AS Date), CAST(N'2022-05-11' AS Date))
INSERT members (membership_id, client_id, name, date_of_membership, expriy_of_membership) VALUES (2015002, 5006, N'akbar', CAST(N'2015-08-09' AS Date), CAST(N'2022-05-11' AS Date))
INSERT members (membership_id, client_id, name, date_of_membership, expriy_of_membership) VALUES (2015003, 5007, N'alina', CAST(N'2012-01-09' AS Date), CAST(N'2022-05-21' AS Date))


INSERT Movie (DvdId, Title, Genre, Release_Date, Producer, Format, For_delivery, Price) VALUES (1011, N'We Bear Bears', N'Children', CAST(N'2015-11-27' AS Date), N'Daniel Chong', N'DVD', N'Available', 450)
INSERT Movie (DvdId, Title, Genre, Release_Date, Producer, Format, For_delivery, Price) VALUES (1012, N'Fast & Furious', N'Action', CAST(N'2021-09-25' AS Date), N'Vin Diesel', N'Blu-ray(Special Edition)', N'Available', 980)
INSERT Movie (DvdId, Title, Genre, Release_Date, Producer, Format, For_delivery, Price) VALUES (1013, N'The Lego', N'Family', CAST(N'2021-02-25' AS Date), N'Rick Rubin', N'Blu-ray', N'Out of stock', 399)
INSERT Movie (DvdId, Title, Genre, Release_Date, Producer, Format, For_delivery, Price) VALUES (1014, N'Deadwood', N'Western', CAST(N'2021-05-25' AS Date), N'George Martin', N'Blu-ray(Digital HD)', N'Out of Stock', 1050)
INSERT Movie (DvdId, Title, Genre, Release_Date, Producer, Format, For_delivery, Price) VALUES (1015, N'Jaws', N'Action', CAST(N'2016-06-25' AS Date), N'Spike Lee', N'Blu-ray', N'Available', 560)



INSERT Mystery (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (10, 425235229, N'A Killer Plot', N'Ellery Adams', N'Berkley Books', N'English', 590)
INSERT Mystery (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (10, 425245004, N'The Last Word', N'Ellery Adams', N' Berkley Books', N'English', 3450)
INSERT Mystery (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (10, 425270831, N'Lethal Letters', N'Ellery Adams', N'Berkley Books', N'English', 690)
INSERT Mystery (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (10, 756405025, N'Blood Trail', N'Tanya Huff', N'Daw Books', N'English', 3450)
INSERT Mystery (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (10, 1538752824, N'The Red Book', N'David Ellis', N'Grand Central Publishing', N'English', 350)


INSERT order_generated (order_id, supplier_id, amount, quantity_of_items, date) VALUES (9901, 2102, 990, 10, CAST(N'2012-01-05' AS Date))
INSERT order_generated (order_id, supplier_id, amount, quantity_of_items, date) VALUES (9902, 2102, 999, 10, CAST(N'2012-05-12' AS Date))
INSERT order_generated (order_id, supplier_id, amount, quantity_of_items, date) VALUES (9903, 2101, 1000, 20, CAST(N'2017-08-12' AS Date))


INSERT orders (order_id, client_id, item_id, item_name,isbn, book_name, total_bill, date) VALUES (19001, 3002, 10011, N'abc-journal', 1709246, N'eating disorder', 2650, CAST(N'2022-04-05' AS Date))
INSERT orders (order_id, client_id, item_id, item_name, isbn, book_name, total_bill, date) VALUES (19002, 3005, NULL, NULL, 1936322, N'selp-help', 2650, CAST(N'2022-04-05' AS Date))
INSERT orders (order_id, client_id, item_id, item_name, isbn, book_name, total_bill, date) VALUES (19003, 3002, 10013, N'spiral-journal', 1709247, N'self esteem', 3550, CAST(N'2022-04-06' AS Date))
INSERT orders (order_id, client_id, item_id, item_name, isbn, book_name, total_bill, date) VALUES (19004, 3006, NULL, NULL, 1813326, N'dracula', 780, CAST(N'2022-04-05' AS Date))


INSERT Poetry (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (16, 97969461, N'MELI MELI DHOOP', N'Anwar Masood', N'Book Corner', N'Urdu', 220)
INSERT Poetry (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (16, 978969462, N'ROZ BA ROZ', N'Anwar Masood', N'Book Corner', N'Urdu', 300)
INSERT Poetry (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (16, 978969463, N'Darpaish', N'Anwar Masood', N'Book Corner', N'Urdu', 250)
INSERT Poetry (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (16, 979508666, N'Black Widow', N'Sadat Hasan Manto', N'Sang e Meel', N'Urdu', 980)
INSERT Poetry (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (16, 979693510, N'A Manto Panorama', N'Sadat Hasan Manto', N'Sang e Meel', N'Urdu', 895)


INSERT Promotions (PromoId, Promo_Name, ISBN, Book_Name, Original_Price, Discounted_Price, Gift) VALUES (20101, N'independence day', 97815098, N'the wich kind', 890, 790, NULL)
INSERT Promotions (PromoId, Promo_Name, ISBN, Book_Name, Original_Price, Discounted_Price, Gift) VALUES (20102, N'10th aniversery', 399592520, N'dead to lead', 5632, 4999, N'choclate')
INSERT Promotions (PromoId, Promo_Name, ISBN, Book_Name, Original_Price, Discounted_Price, Gift) VALUES (20103, N'10th aniversery', 393541215, N'the work', 5000, 4599, N'choclate')


INSERT Publisher (PublisherID, Name) VALUES (2001, N'Simon & Schuster')
INSERT Publisher (PublisherID, Name) VALUES (2002, N'National Geographic Society')
INSERT Publisher (PublisherID, Name) VALUES (2003, N'Grand Central Publishing')
INSERT Publisher (PublisherID, Name) VALUES (2004, N'Darul Musannefin Shibli')
INSERT Publisher (PublisherID, Name) VALUES (2005, N'NationalBureau of Publications')
INSERT Publisher (PublisherID, Name) VALUES (2006, N'Random House')
INSERT Publisher (PublisherID, Name) VALUES (2007, N'Ramsey Press')
INSERT Publisher (PublisherID, Name) VALUES (2008, N'Wiley')
INSERT Publisher (PublisherID, Name) VALUES (2009, N'Portfolio')
INSERT Publisher (PublisherID, Name) VALUES (2010, N'HarperCollins Leadership')
INSERT Publisher (PublisherID, Name) VALUES (2011, N'Oxford')
INSERT Publisher (PublisherID, Name) VALUES (2012, N'Harpor Brothers')
INSERT Publisher (PublisherID, Name) VALUES (2013, N'Arbor Publishing')
INSERT Publisher (PublisherID, Name) VALUES (2014, N'Sang e Meel')
INSERT Publisher (PublisherID, Name) VALUES (2015, N'Macmillan')
INSERT Publisher (PublisherID, Name) VALUES (2016, N'Hachette Book Group')
INSERT Publisher (PublisherID, Name) VALUES (2017, N'Penguin USA')
INSERT Publisher (PublisherID, Name) VALUES (2018, N'Norton & Company')





INSERT recipt (recipt_id, client_id, membership_id, amount_charge, date) VALUES (15001, 3001, NULL, 499, CAST(N'2017-02-03' AS Date))
INSERT recipt (recipt_id, client_id, membership_id, amount_charge, date) VALUES (15002, NULL, 2015001, 2999, CAST(N'2018-03-04' AS Date))
INSERT recipt (recipt_id, client_id, membership_id, amount_charge, date) VALUES (15003, 3004, NULL, 199, CAST(N'2019-04-07' AS Date))
INSERT recipt (recipt_id, client_id, membership_id, amount_charge, date) VALUES (15004, 3005, NULL, 2299, CAST(N'2020-06-08' AS Date))


INSERT Romance (CategoryId, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (13, 62353659, N'Bridgerton', N'Julia Quinn', N'Avon Books', N'English', 1600)
INSERT Romance (CategoryId, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (13, 1476792488, N'After', N'Anna Todd', N'Gallery Books', N'English', 2090)
INSERT Romance (CategoryId, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (13, 1501110365, N'It Ends with Us', N'Collen Hoover', N'Atria Books', N'English', 3478)
INSERT Romance (CategoryId, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (13, 1538728621, N'The Wish', N'Nicholas Sparks', N'Grand Central Publishing', N'English', 980)
INSERT Romance (CategoryId, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (13, 1668001225, N'It Starts with Us', N'Collen Hoover', N'Atria Books', N'English', 1356)


INSERT Sci_Fi (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (17, 441172717, N'Dune', N'Frank Herbert', N'Ace Books', N'English', 560)
INSERT Sci_Fi (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (17, 451464419, N'Peace Talks', N'Jim Butcher', N'Ace Books', N'English', 5900)
INSERT Sci_Fi (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (17, 765394863, N'Ender Game', N'Orson Scott', N'Avon Books', N'English', 1600)
INSERT Sci_Fi (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (17, 1250788838, N'Siren Queen', N'Nghi Vo', N'Tordotcom', N'English', 4560)
INSERT Sci_Fi (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (17, 1338732870, N'The Ickabog', N'J.K. Rowling', N'Scholastic', N'English', 300)


INSERT Science (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (11, 978053176, N'A Brief History', N'Stephen Hawking', N'Simon & Schuster', N'English', 8980)
INSERT Science (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (11, 978053177, N'The Grand Design', N'Stephen Hawking', N'Simon & Schuster', N'English', 7500)
INSERT Science (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (11, 978053178, N'The Universe In A Nutshell', N'Stephen Hawking', N'Simon & Schuster', N'English', 8208)
INSERT Science (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (11, 978053179, N'Big Questions', N'Stephen Hawking', N'Simon & Schuster', N'English', 8395)
INSERT Science (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (11, 978053180, N'Unlocking the Universe', N'Stephen Hawking', N'Simon & Schuster', N'English', 9840)
INSERT Self_Help (CategoryId, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (12, 1709246, N'Eating Disorder', N'James Glad', N'Daw Books', N'English', 2580)
INSERT Self_Help (CategoryId, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (12, 1709247, N'Self Esteem', N'James Glad', N'Daw Books', N'English', 3500)
INSERT Self_Help (CategoryId, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (12, 1709248, N'Help Your Self!', N'James Glad', N'Daw Books', N'English', 2208)
INSERT Self_Help (CategoryId, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (12, 1936320, N'The Myth of Self Help', N'Gerald Alper', N'Berkley Books', N'English', 8395)
INSERT Self_Help (CategoryId, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (12, 1936322, N'Self-Help Manual', N'Gerald Alper', N'Berkley Books', N'English', 9840)










INSERT Staff (StaffID, Name, DateOfJoining, Salary, Address, DeparmentID, DepartmentName) VALUES (12001, N'aslam', 21, 21000, N'ls-5 sector 7 c nk', 3001, N'sales')
INSERT Staff (StaffID, Name, DateOfJoining, Salary, Address, DeparmentID, DepartmentName) VALUES (12002, N'ramis', 21, 28000, N'ls-5 sector 7 c nk', 3002, N'marketing')
INSERT Staff (StaffID, Name, DateOfJoining, Salary, Address, DeparmentID, DepartmentName) VALUES (12003, N'romaisa', 21, 20000, N'ls-5 sector 7 c nk', 3003, N'store-keeping')


INSERT Supplier (SupplierId, Name, Address, Phone, Email) VALUES (2101, N'kareem', N'store-no. 9 street markte LA', 3902990, N'lari@gmail.com')
INSERT Supplier (SupplierId, Name, Address, Phone, Email) VALUES (2102, N'areeba', N'store-no. 10 street markte LA', 3902990, N'areei@gmail.com')


INSERT Crime (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (15, 316419486, N'The Witch Kind', N'Louisa Morgan', N'Redhook', N'English', 6777)
INSERT Crime (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (15, 316508586, N'A Secret History of Witches', N'Louisa Morgan', N'Redhook', N'English', 3450)
INSERT Crime (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (15, 1250160839, N'Mrs. Sherlock Holmes', N'Brad Ricca', N'Redhook', N'English', 1430)
INSERT Crime (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (15, 1250622794, N'Unmasked', N'Susan Jonusas', N'Viking', N'English', 3450)
INSERT Crime (Category_Id, ISBN, Book_Name, Author_Name, Publisher_Name, Language, Price) VALUES (15, 1984879839, N'Hell is Half-Acre', N'Susan Jonusas', N'Viking', N'English', 1999)

INSERT walk_incustomer (client_id, name, contact, email) VALUES (3001, N'akram', N'031255123', N'akri@gmail.com')
INSERT walk_incustomer (client_id, name, contact, email) VALUES (3002, N'shakir', N'0131255123', N'shakri@gmail.com')
INSERT walk_incustomer (client_id, name, contact, email) VALUES (3003, N'younus', N'06546523', N'talahyounus@gmail.com')
INSERT walk_incustomer (client_id, name, contact, email) VALUES (3004, N'aslam', N'031255123', N'akri@gmail.com')
INSERT walk_incustomer (client_id, name, contact, email) VALUES (3005, N'jimi', N'03546463', N'jamal@gmail.com')
INSERT walk_incustomer (client_id, name, contact, email) VALUES (3006, N'areeba', N'03154623', N'ariba@gmail.com')


INSERT WholeSeller (WholeSellerId, Name, Address, Phone, Email) VALUES (3001, N'haider', N'ls-67 sector 5 a 2 state LA', 30124567, N'haider@outlook.com')


ALTER TABLE Business  WITH CHECK ADD  CONSTRAINT [FK_Catid2] FOREIGN KEY(Category_Id)
REFERENCES Category (Category_Id)

ALTER TABLE books  WITH CHECK ADD FOREIGN KEY(category_id)
REFERENCES Category (Category_Id)

ALTER TABLE Biography  WITH CHECK ADD  CONSTRAINT [FK_Cat_id1] FOREIGN KEY(Category_Id)
REFERENCES Category (Category_Id)

ALTER TABLE bills_paid  WITH CHECK ADD FOREIGN KEY(supplier_id)
REFERENCES Supplier (SupplierId)

ALTER TABLE bills_paid  WITH CHECK ADD FOREIGN KEY(supplier_id)
REFERENCES Supplier(SupplierId)

ALTER TABLE bills_paid  WITH CHECK ADD FOREIGN KEY(order_id)
REFERENCES order_generated (order_id)

ALTER TABLE Biography CHECK CONSTRAINT [FK_Cat_id1]

ALTER TABLE bills_paid  WITH CHECK ADD FOREIGN KEY(order_id)
REFERENCES order_generated (order_id)

SELECT DISTINCT publisher_id
FROM books
WHERE publisher_id NOT IN (SELECT PublisherID FROM Publisher);

DELETE FROM books
WHERE publisher_id NOT IN (SELECT PublisherID FROM Publisher);

ALTER TABLE books
WITH CHECK ADD CONSTRAINT FK_books_publisher
FOREIGN KEY (publisher_id) REFERENCES Publisher(PublisherID);

ALTER TABLE books
WITH CHECK CHECK CONSTRAINT FK_books_publisher;




ALTER TABLE books  WITH CHECK ADD FOREIGN KEY(author_id)
REFERENCES Author (AuthorID)

ALTER TABLE audio_book  WITH CHECK ADD FOREIGN KEY(category_id)
REFERENCES Category (Category_Id)
ALTER TABLE Afsanay  WITH CHECK ADD  CONSTRAINT [FK_Catid18] FOREIGN KEY(CategoryId)
REFERENCES Category (Category_Id)


SELECT COLUMN_NAME
FROM INFORMATION_SCHEMA.COLUMNS
WHERE TABLE_NAME = 'Admin';

BEGIN TRY
    ALTER TABLE Admin
    ADD Admin_Id INT; 
    PRINT 'Column Admin_Id added to Admin table.';
END TRY
BEGIN CATCH
    PRINT 'Column Admin_Id already exists or failed to add.';
END CATCH;


BEGIN TRY
    ALTER TABLE Admin_Login
    WITH CHECK ADD CONSTRAINT FK_Admin_Login_Admin
    FOREIGN KEY (AdminId) REFERENCES Admin(Admin_Id);
    PRINT 'Foreign key constraint added successfully.';
END TRY
BEGIN CATCH
    PRINT 'Failed to add foreign key constraint.';
END CATCH;
SELECT name AS ConstraintName
FROM sys.foreign_keys
WHERE parent_object_id = OBJECT_ID('Admin_Login');

ALTER TABLE Business CHECK CONSTRAINT [FK_Catid2]

ALTER TABLE Children  WITH CHECK ADD  CONSTRAINT [FK_Catid3] FOREIGN KEY(Category_Id)
REFERENCES Category (Category_Id)

ALTER TABLE Children CHECK CONSTRAINT [FK_Catid3]

ALTER TABLE Comics  WITH CHECK ADD  CONSTRAINT [FK_Catid4] FOREIGN KEY(Category_Id)
REFERENCES Category (Category_Id)

ALTER TABLE Comics CHECK CONSTRAINT [FK_Catid4]

ALTER TABLE contact_staff  WITH CHECK ADD FOREIGN KEY(staff_id)
REFERENCES Staff (StaffID)

ALTER TABLE Cook_Books  WITH CHECK ADD  CONSTRAINT [FK_Catid5] FOREIGN KEY(Category_Id)
REFERENCES Category ([Category_Id])

ALTER TABLE Cook_Books CHECK CONSTRAINT [FK_Catid5]

ALTER TABLE Events  WITH CHECK ADD FOREIGN KEY(AuthorID)
REFERENCES Author (AuthorID)

ALTER TABLE Fantasy  WITH CHECK ADD  CONSTRAINT [FK_Catid6] FOREIGN KEY(Category_Id)
REFERENCES Category (Category_Id)

ALTER TABLE Fantasy CHECK CONSTRAINT [FK_Catid6]

ALTER TABLE Fiction  WITH CHECK ADD  CONSTRAINT [FK_Catid14] FOREIGN KEY(Category_Id)
REFERENCES Category (Category_Id)

ALTER TABLE Fiction CHECK CONSTRAINT [FK_Catid14]

ALTER TABLE History  WITH CHECK ADD  CONSTRAINT [FK_Catid7] FOREIGN KEY(Category_Id)
REFERENCES Category (Category_Id)

ALTER TABLE History CHECK CONSTRAINT [FK_Catid7]

ALTER TABLE Horror  WITH CHECK ADD  CONSTRAINT [FK_Catid8] FOREIGN KEY(Category_Id)
REFERENCES Category (Category_Id)

ALTER TABLE Horror CHECK CONSTRAINT [FK_Catid8]

ALTER TABLE Humor  WITH CHECK ADD  CONSTRAINT [FK_Catid9] FOREIGN KEY(Category_Id)
REFERENCES Category (Category_Id)

ALTER TABLE Humor CHECK CONSTRAINT [FK_Catid9]

ALTER TABLE Items  WITH CHECK ADD FOREIGN KEY(company_id)
REFERENCES Company (CompanyId)

ALTER TABLE Items  WITH CHECK ADD FOREIGN KEY(item_category)
REFERENCES item_category (item_c_id)

ALTER TABLE Items  WITH CHECK ADD FOREIGN KEY(whole_seller_id)
REFERENCES WholeSeller (WholeSellerId)

ALTER TABLE member_info  WITH CHECK ADD FOREIGN KEY(membership_id)
REFERENCES members (membership_id)

ALTER TABLE Mystery  WITH CHECK ADD  CONSTRAINT [FK_Catid10] FOREIGN KEY(Category_Id)
REFERENCES Category (Category_Id)

ALTER TABLE Mystery CHECK CONSTRAINT [FK_Catid10]

ALTER TABLE order_generated  WITH CHECK ADD FOREIGN KEY(supplier_id)
REFERENCES Supplier (SupplierId)

ALTER TABLE orders  WITH CHECK ADD FOREIGN KEY(client_id)
REFERENCES walk_incustomer (client_id)




ALTER TABLE orders  WITH CHECK ADD FOREIGN KEY(isbn)
REFERENCES books (isbn)

ALTER TABLE orders  WITH CHECK ADD FOREIGN KEY(item_id)
REFERENCES Items (item_id)

ALTER TABLE Poetry  WITH CHECK ADD  CONSTRAINT [FK_Catid16] FOREIGN KEY(Category_Id)
REFERENCES Category (Category_Id)

ALTER TABLE Poetry CHECK CONSTRAINT [FK_Catid16]

ALTER TABLE Promotions  WITH CHECK ADD FOREIGN KEY(ISBN)
REFERENCES books (isbn)

ALTER TABLE recipt  WITH CHECK ADD FOREIGN KEY(client_id)
REFERENCES walk_incustomer(client_id)

ALTER TABLE Romance WITH CHECK ADD  CONSTRAINT [FK_Catid13] FOREIGN KEY(CategoryId)
REFERENCES Category (Category_Id)

ALTER TABLE Romance CHECK CONSTRAINT [FK_Catid13]

ALTER TABLE Sci_Fi  WITH CHECK ADD  CONSTRAINT [FK_Catid17] FOREIGN KEY(Category_Id)
REFERENCES Category (Category_Id)

ALTER TABLE Sci_Fi CHECK CONSTRAINT [FK_Catid17]

ALTER TABLE Science  WITH CHECK ADD  CONSTRAINT [FK_Catid11] FOREIGN KEY(Category_Id)
REFERENCES Category (Category_Id)

ALTER TABLE Science CHECK CONSTRAINT [FK_Catid11]

ALTER TABLE Self_Help  WITH CHECK ADD  CONSTRAINT [FK_Catid12] FOREIGN KEY(CategoryId)
REFERENCES Category (Category_Id)

ALTER TABLE Self_Help CHECK CONSTRAINT [FK_Catid12]



ALTER TABLE Staff WITH CHECK ADD FOREIGN KEY(DeparmentID)
REFERENCES Department (DeptId)

ALTER TABLE Crime  WITH CHECK ADD  CONSTRAINT [FK_Catid15] FOREIGN KEY(Category_Id)
REFERENCES Category (Category_Id)

ALTER TABLE Crime CHECK CONSTRAINT [FK_Catid15]

USE [bookstore]

ALTER DATABASE [bookstore] SET  READ_WRITE 






