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

# _WSMAN_DATA structure


## -description


Contains inbound and outbound data used in the Windows Remote Management (WinRM) API.


## -struct-fields




### -field type

Specifies the type of data currently stored in the union.


### -field text

 


### -field binaryData

 


### -field number

 




#### - ( unnamed union )

Contains the data.



#### text

If <b>type</b> is <b>WSMAN_DATA_TYPE_TEXT</b>,  <b>text</b> contains a <a href="https://msdn.microsoft.com/463dcc6a-2a56-42a9-a778-7a634e5f977c">WSMAN_DATA_TEXT</a> structure.



#### binaryData

If <b>type</b> is <b>WSMAN_DATA_TYPE_XML_BINARY</b>, <b>binaryData</b> contains a <a href="https://msdn.microsoft.com/35beedc3-30c6-4e04-bc27-bb9eb21256fe">WSMAN_DATA_BINARY</a> structure.



#### number

If <b>type</b> is <b>WSMAN_DATA_TYPE_DWORD</b>, <b>number</b> is a DWORD integer.

