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

# IShellItemResources::GetAttributes


## -description


Gets resource attributes.


## -parameters




### -param pdwAttributes [out]

Type: <b>DWORD*</b>

A pointer to resource attributes. The following are attribute values.



#### FILE_ATTRIBUTE_READONLY

Value is 0x00000001.



#### FILE_ATTRIBUTE_HIDDEN

Value is 0x00000002.



#### FILE_ATTRIBUTE_SYSTEM

Value is 0x00000004.



#### FILE_ATTRIBUTE_DIRECTORY

Value is 0x00000010.



#### FILE_ATTRIBUTE_ARCHIVE

Value is 0x00000020.



#### FILE_ATTRIBUTE_ENCRYPTED

Value is 0x00000040.



#### FILE_ATTRIBUTE_NORMAL

Value is 0x00000080.



#### FILE_ATTRIBUTE_TEMPORARY

Value is 0x00000100.



#### FILE_ATTRIBUTE_SPARSE_FILE

Value is 0x00000200.



#### FILE_ATTRIBUTE_REPARSE_POINT

Value is 0x00000400.



#### FILE_ATTRIBUTE_COMPRESSED

Value is 0x00000800.



#### FILE_ATTRIBUTE_OFFLINE

Value is 0x00001000.



#### FILE_ATTRIBUTE_CONTENT_INDEXED

Value is 0x00002000.



#### FILE_ATTRIBUTE_VALID_FLAGS

Value is 0x00001ff7.



#### FILE_ATTRIBUTE_VALID_SET_FLAGS

Value is 0x000011a7.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



