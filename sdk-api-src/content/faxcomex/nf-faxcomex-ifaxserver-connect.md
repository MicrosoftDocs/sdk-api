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

# IFaxServer::Connect


## -description


The <b>Connect</b> method connects a fax client application to the specified fax server.



## -parameters




### -param bstrServerName

Type: <b>String</b>

A null-terminated string that specifies the name of the target fax server, such as "computername". If this parameter is <b>Null</b> or an empty string, the method connects the application to the fax server on the local computer.


## -remarks



Before accessing most of the objects of the fax extended Component Object Model (COM), the application must call this method to initiate a connection with an active fax server. A fax server connection is not required for you to access a <a href="https://msdn.microsoft.com/a87e6de7-1541-4f9e-b411-d8c6907bf93e">FaxDocument</a> object. The method fails if the client is not connected to an active fax server. 

To connect to the local server, set the <i>bstrServerName</i> parameter to <b>Null</b> or an empty string. For usage examples, see <a href="https://msdn.microsoft.com/aa3cd5cf-fff5-453b-9574-7ef617239da6">Connecting to the Fax Server</a>.




## -see-also




<a href="https://msdn.microsoft.com/df3aa427-9d29-4024-a6d5-ed5fd8dba36c">FaxServer</a>



<a href="https://msdn.microsoft.com/9e8718b9-f957-43c4-92de-f320aa42a096">IFaxServer</a>



<a href="https://msdn.microsoft.com/80437d99-5b9f-4faa-8f09-ed91fc622d4b">Visual Basic Example</a>
 

 

