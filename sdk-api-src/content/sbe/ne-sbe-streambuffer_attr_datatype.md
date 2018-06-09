---
UID: NE:sbe.STREAMBUFFER_ATTR_DATATYPE
title: STREAMBUFFER_ATTR_DATATYPE
author: windows-sdk-content
description: This topic applies only to Windows XP Service Pack 1 or later.
old-location: mstv\streambuffer_attr_datatype.htm
old-project: mstv
ms.assetid: be478769-d9ac-4e42-b5f6-94b5656e2596
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: STREAMBUFFER_ATTR_DATATYPE, STREAMBUFFER_ATTR_DATATYPE , STREAMBUFFER_ATTR_DATATYPE enumeration [Microsoft TV Technologies], STREAMBUFFER_ATTR_DATATYPEEnumeration, STREAMBUFFER_TYPE_BINARY, STREAMBUFFER_TYPE_BOOL, STREAMBUFFER_TYPE_DWORD, STREAMBUFFER_TYPE_GUID, STREAMBUFFER_TYPE_QWORD, STREAMBUFFER_TYPE_STRING, STREAMBUFFER_TYPE_WORD, mstv.streambuffer_attr_datatype, sbe/STREAMBUFFER_ATTR_DATATYPE, sbe/STREAMBUFFER_TYPE_BINARY, sbe/STREAMBUFFER_TYPE_BOOL, sbe/STREAMBUFFER_TYPE_DWORD, sbe/STREAMBUFFER_TYPE_GUID, sbe/STREAMBUFFER_TYPE_QWORD, sbe/STREAMBUFFER_TYPE_STRING, sbe/STREAMBUFFER_TYPE_WORD
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: sbe.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: STREAMBUFFER_ATTR_DATATYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sbe.h
api_name:
 - STREAMBUFFER_ATTR_DATATYPE
product: Windows
targetos: Windows
req.lib: Sas.lib
req.dll: Sas.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

