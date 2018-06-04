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

# SendToFaxRecipient function


## -description


Called by an application to fax a file. 


## -parameters




### -param sndMode

Type: <b><a href="https://msdn.microsoft.com/6b9e75b2-1a79-4056-b3c8-215cb3e975b1">SendToMode</a></b>

A value specifying how to send the fax. For Windows Vista, this must be <a href="https://msdn.microsoft.com/6b9e75b2-1a79-4056-b3c8-215cb3e975b1">SEND_TO_FAX_RECIPIENT_ATTACHMENT</a>.


### -param lpFileName

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated string representing the name of the file to fax. 


## -returns



Type: <b>DWORD</b>

Zero, if the operation is successful.




## -remarks




        Call <a href="https://msdn.microsoft.com/88f74423-f9dd-4846-a53a-a24ff08048d3">CanSendToFaxRecipient</a> first to determine if faxing from within an application is possible on the computer.  
        




## -see-also




<a href="https://msdn.microsoft.com/88f74423-f9dd-4846-a53a-a24ff08048d3">CanSendToFaxRecipient</a>



<a href="https://msdn.microsoft.com/6b9e75b2-1a79-4056-b3c8-215cb3e975b1">SendToMode</a>



<a href="https://msdn.microsoft.com/555ee494-ee1c-4047-b7ae-a890176a6b32">Shell Fax Extension Functions</a>
 

 

