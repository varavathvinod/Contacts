# Contacts
1. Create SQL DB Called - Contact
2. Execute below script - 
USE [Contact]
GO

/****** Object:  Table [dbo].[Contact]    Script Date: 04-07-2021 05:50:55 ******/
SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE [dbo].[Contact](
	[ID] [int] IDENTITY(1,1) NOT NULL,
	[FirstName] [varchar](25) NOT NULL,
	[LastName] [varchar](25) NOT NULL,
	[Email] [varchar](50) NOT NULL,
	[PhoneNumber] [varchar](20) NOT NULL,
	[Status] [bit] NOT NULL,
 CONSTRAINT [PK_ContactDetails] PRIMARY KEY CLUSTERED 
(
	[ID] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON, OPTIMIZE_FOR_SEQUENTIAL_KEY = OFF) ON [PRIMARY]
) ON [PRIMARY]
GO
4. Unzip the attached .rar file
5. Change the sql connection in appsettings
6. Open "nlog.config" with the new log path <target name="logfile" xsi:type="File" fileName="D:/Logs/${shortdate}_log.txt" layout="${longdate} ${level:uppercase=true} ${message}"/>
