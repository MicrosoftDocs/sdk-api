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

# _WSANSClassInfoW structure


## -description


The <b>WSANSCLASSINFO</b> structure provides individual parameter information for a specific Windows Sockets namespace.


## -struct-fields




### -field lpszName

String value associated with the parameter, such as SAPID, TCPPORT, and so forth.


### -field dwNameSpace

GUID associated with the namespace.


### -field dwValueType

Value type for the parameter, such as REG_DWORD or REG_SZ, and so forth.


### -field dwValueSize

Size of the parameter provided in <b>lpValue</b>, in bytes.


### -field lpValue

Pointer to the value of the parameter.


## -remarks



The <b>WSANSCLASSINFO</b> structure is defined differently depending on whether ANSI or UNICODE is used. The above syntax block applies to ANSI; for UNICODE, the datatype for <b>lpszName</b> is <b>LPWSTR</b>.




## -see-also




<a href="https://msdn.microsoft.com/02422c24-34a6-4e34-a795-66b0b687ac44">WSASERVICECLASSINFO</a>
 

 

