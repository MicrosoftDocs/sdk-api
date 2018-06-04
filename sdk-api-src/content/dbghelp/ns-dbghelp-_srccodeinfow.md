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

# _SRCCODEINFOW structure


## -description


Contains line information.


## -struct-fields




### -field SizeOfStruct

The size of the structure, in bytes.


### -field Key

This member is not used.


### -field ModBase

The base address of the module that contains the line.


### -field Obj

The name of the object file within the module that contains the line.


### -field FileName

The fully qualified source file name.


### -field LineNumber

The line number within the source file.


### -field Address

The virtual address of the first instruction of the line.


## -see-also




<a href="https://msdn.microsoft.com/7379dd04-72a4-45b6-b02a-d3e8a5aaf0d7">SymEnumLinesProc</a>
 

 

