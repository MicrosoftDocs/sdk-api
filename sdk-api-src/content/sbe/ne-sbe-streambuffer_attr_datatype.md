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

# STREAMBUFFER_ATTR_DATATYPE enumeration


## -description



This topic applies only to Windows XP Service Pack 1 or later.
        



The <b>STREAMBUFFER_ATTR_DATATYPE</b> enumeration defines the data type for an attribute.


## -enum-fields




### -field STREAMBUFFER_TYPE_DWORD

The attribute is a 32-bit <b>DWORD</b> value.


### -field STREAMBUFFER_TYPE_STRING

The attribute is a null-terminated wide-character string.


### -field STREAMBUFFER_TYPE_BINARY

The attribute is an array of bytes.


### -field STREAMBUFFER_TYPE_BOOL

The attribute is a 32-bit Boolean value.


### -field STREAMBUFFER_TYPE_QWORD

The attribute is a 64-bit <b>QWORD</b> value.


### -field STREAMBUFFER_TYPE_WORD

The attribute is a 16-bit <b>WORD</b> value.


### -field STREAMBUFFER_TYPE_GUID

The attribute is a 128-bit <b>GUID</b> value.


## -see-also




<a href="https://msdn.microsoft.com/7c46413f-3e51-4d72-b7f7-a8239c61b161">IStreamBufferRecordingAttribute Interface</a>



<a href="https://msdn.microsoft.com/2b17626a-9268-4192-8acf-ed46bf632163">STREAMBUFFER_ATTRIBUTE Structure</a>



<a href="https://msdn.microsoft.com/36cd9e1c-daca-428b-96c7-f50c31d5ba4c">Stream Buffer Engine Enumeration Types</a>
 

 

