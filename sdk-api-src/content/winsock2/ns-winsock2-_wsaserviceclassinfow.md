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

# _WSAServiceClassInfoW structure


## -description



			The 
<b>WSASERVICECLASSINFO</b> structure contains information about a specified service class. For each service class in Windows Sockets 2, there is a single 
<b>WSASERVICECLASSINFO</b> structure.


## -struct-fields




### -field lpServiceClassId

Unique Identifier (GUID) for the service class.


### -field lpszServiceClassName

Well known name associated with the service class.


### -field dwCount

Number of entries in <b>lpClassInfos</b>.


### -field lpClassInfos

Array of <a href="https://msdn.microsoft.com/b4f811ad-7967-45bd-b563-a28bb1633596">WSANSCLASSINFO</a> structures that contains information about the service class.


## -see-also




<a href="https://msdn.microsoft.com/babe1c96-9077-4d91-a52a-839c89d7a83b">NSPGetServiceClassInfo</a>



<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPLookupServiceBegin</a>
 

 

