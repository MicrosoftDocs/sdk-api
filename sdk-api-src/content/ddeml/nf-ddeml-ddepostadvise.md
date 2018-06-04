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

# DdePostAdvise function


## -description


Causes the system to send an <a href="https://msdn.microsoft.com/9bd43e61-cbd6-4d53-bab3-90e85819b16b">XTYP_ADVREQ</a> transaction to the calling (server) application's Dynamic Data Exchange (DDE) callback function for each client with an active advise loop on the specified topic and item. A server application should call this function whenever the data associated with the topic name or item name pair changes. 


## -parameters




### -param idInst [in]

Type: <b>DWORD</b>

The application instance identifier obtained by a previous call to the <a href="https://msdn.microsoft.com/ea679d2b-8c03-4706-b6a8-37a99c6d61d1">DdeInitialize</a> function. 


### -param hszTopic [in]

Type: <b>HSZ</b>

A handle to a string that specifies the topic name. To send notifications for all topics with active advise loops, an application can set this parameter to 0L. 


### -param hszItem [in]

Type: <b>HSZ</b>

A handle to a string that specifies the item name. To send notifications for all items with active advise loops, an application can set this parameter to 0L. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 

The <a href="https://msdn.microsoft.com/ea7d758e-bf88-49a9-a51f-9be26376a1ed">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values:




## -remarks



A server that has nonenumerable topics or items should set the 
				<i>hszTopic</i> and 
				<i>hszItem</i> parameters to <b>NULL</b> so that the system generates transactions for all active advise loops. The server's DDE callback function returns <b>NULL</b> for any advise loops that must not be updated. 

If a server calls <b>DdePostAdvise</b> with a topic, item, and format name set that includes the set currently being handled in an <a href="https://msdn.microsoft.com/9bd43e61-cbd6-4d53-bab3-90e85819b16b">XTYP_ADVREQ</a> callback, a stack overflow can result. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/ea679d2b-8c03-4706-b6a8-37a99c6d61d1">DdeInitialize</a>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/9bd43e61-cbd6-4d53-bab3-90e85819b16b">XTYP_ADVREQ</a>
 

 

