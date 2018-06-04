---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _FAX_COVERPAGE_INFOA structure


## -description


The <b>FAX_COVERPAGE_INFO</b> structure contains data to display on the cover page of a fax transmission. The <b>SizeOfStruct</b> and <b>CoverPageName</b> members are required; other members are optional.


## -struct-fields




### -field SizeOfStruct

Type: <b>DWORD</b>

Specifies the size, in bytes, of the <b>FAX_COVERPAGE_INFO</b> structure. The calling application must set this member to <b>sizeof(FAX_COVERPAGE_INFO)</b>.


### -field CoverPageName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the name of the cover page file (.cov) to associate with the received fax document. The string can be the file name of the common cover page file, or it can be the UNC path to a local cover page file. 



### -field UseServerCoverPage

Type: <b>BOOL</b>

Specifies a Boolean variable that indicates whether the fax cover page file is stored on the local computer or in the common cover page location. A value of <b>TRUE</b> indicates that the cover page file resides in the common cover page location on the fax server.


### -field RecName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the name of the recipient of the fax transmission.


### -field RecFaxNumber

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the fax number of the recipient of the fax transmission. 



### -field RecCompany

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the company name of the recipient of the fax transmission.


### -field RecStreetAddress

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the street address of the recipient of the fax transmission.


### -field RecCity

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the city of the recipient of the fax transmission.


### -field RecState

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the state of the recipient of the fax transmission. 



### -field RecZip

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the postal ZIP code of the recipient of the fax transmission. 



### -field RecCountry

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the country/region of the recipient of the fax transmission. 



### -field RecTitle

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the title of the recipient of the fax transmission. 



### -field RecDepartment

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the department of the recipient of the fax transmission. 



### -field RecOfficeLocation

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the office location of the recipient of the fax transmission. 



### -field RecHomePhone

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the home telephone number of the recipient of the fax transmission. 



### -field RecOfficePhone

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the office telephone number of the recipient of the fax transmission. 



### -field SdrName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the name of the sender who initiated the fax transmission. 



### -field SdrFaxNumber

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the fax number of the sender who initiated the fax transmission. 



### -field SdrCompany

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the company name of the sender who initiated the fax transmission. 



### -field SdrAddress

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the address of the sender who initiated the fax transmission. 



### -field SdrTitle

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the title of the sender who initiated the fax transmission. 



### -field SdrDepartment

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the department name of the sender who initiated the fax transmission. 



### -field SdrOfficeLocation

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the office location of the sender who initiated the fax transmission. 



### -field SdrHomePhone

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the home telephone number of the sender who initiated the fax transmission. 



### -field SdrOfficePhone

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the office telephone number of the sender who initiated the fax transmission. 



### -field Note

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that contains the text of a message or note from the sender that pertains to the fax transmission. The text will appear on the cover page. 



### -field Subject

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the subject line of the fax transmission. 



### -field TimeSent

Type: <b><a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a></b>

Specifies a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure. The fax server sets this member when it initiates the fax transmission. The time is expressed in local system time. 



### -field PageCount

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that indicates the total number of pages in the fax transmission. 



## -remarks



A fax client application passes the <b>FAX_COVERPAGE_INFO</b> structure in a call to the <a href="https://msdn.microsoft.com/a48d4eb2-2b49-4379-a281-e5465de1af94">FaxPrintCoverPage</a> function. This enables a user to print a personal cover page at the beginning of a fax transmission. For more information, see <a href="https://msdn.microsoft.com/37bbff77-08a8-486f-ac26-d7b69a936e05">Cover Pages</a> and <a href="https://msdn.microsoft.com/bee4d50b-d6e3-432b-9db6-c7df837079f4">Transmitting Faxes</a>.




## -see-also




<a href="https://msdn.microsoft.com/be81e221-4aba-4c63-9640-337bee49fdb4">Fax Service Client API Structures</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/46eb9960-1d07-4792-83d6-d2f5948e05e9">FaxCompleteJobParams</a>



<a href="https://msdn.microsoft.com/a48d4eb2-2b49-4379-a281-e5465de1af94">FaxPrintCoverPage</a>



<a href="https://msdn.microsoft.com/bbf8def4-4af0-4315-94f9-860f9db1eefa">FaxSendDocument</a>



<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a>
 

 

