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

# EXP_PROPERTYSTORAGE structure


## -description


Stores information about the Shell link state. This structure is used for extra data sections that are tagged with EXP_PROPERTYSTORAGE_SIG.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size of this structure, in bytes.


### -field dwSignature

Type: <b>DWORD</b>

Identifies the type of block and is the value EXP_PROPERTYSTORAGE_SIG.


### -field abPropertyStorage

Type: <b>BYTE[1]</b>

A serialized property store in the format defined by SERIALIZEDPROPSTORAGE.


## -remarks



 EXP_PROPERTYSTORAGE is used to store information serialized by the <a href="https://msdn.microsoft.com/67982d28-27ce-4482-b588-10fec8143750">IShellLink</a> object.  It is named with the tag value EXP_PROPERTYSTORAGE_SIG and can be accessed via <a href="https://msdn.microsoft.com/ac3279ad-1413-48bf-a830-4ec128352573">IShellLinkDataList</a>, including operations for add, remove, and copy. This block can be used to inspect the Shell link state.



