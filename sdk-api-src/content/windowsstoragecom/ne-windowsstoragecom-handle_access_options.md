---
UID: NE:windowsstoragecom.HANDLE_ACCESS_OPTIONS
title: HANDLE_ACCESS_OPTIONS (windowsstoragecom.h)
description: Defines the level of access that a handle has on files.helpviewer_keywords: ["HANDLE_ACCESS_OPTIONS","HANDLE_ACCESS_OPTIONS enumeration [Windows Runtime]","HAO_DELETE","HAO_NONE","HAO_READ","HAO_READ_ATTRIBUTES","HAO_WRITE","windowsstoragecom/HANDLE_ACCESS_OPTIONS","windowsstoragecom/HAO_DELETE","windowsstoragecom/HAO_NONE","windowsstoragecom/HAO_READ","windowsstoragecom/HAO_READ_ATTRIBUTES","windowsstoragecom/HAO_WRITE","winrt.handle_access_options"]
old-location: winrt\handle_access_options.htm
tech.root: WinRT
ms.assetid: C0B140E6-B950-45A9-97BF-5A069BED31FD
ms.date: 12/05/2018
ms.keywords: HANDLE_ACCESS_OPTIONS, HANDLE_ACCESS_OPTIONS enumeration [Windows Runtime], HAO_DELETE, HAO_NONE, HAO_READ, HAO_READ_ATTRIBUTES, HAO_WRITE, windowsstoragecom/HANDLE_ACCESS_OPTIONS, windowsstoragecom/HAO_DELETE, windowsstoragecom/HAO_NONE, windowsstoragecom/HAO_READ, windowsstoragecom/HAO_READ_ATTRIBUTES, windowsstoragecom/HAO_WRITE, winrt.handle_access_options
f1_keywords:
- windowsstoragecom/HANDLE_ACCESS_OPTIONS
dev_langs:
- c++
req.header: windowsstoragecom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- windowsstoragecom.h
api_name:
- HANDLE_ACCESS_OPTIONS
targetos: Windows
req.typenames: HANDLE_ACCESS_OPTIONS
req.redist: 
ms.custom: 19H1
---

# HANDLE_ACCESS_OPTIONS enumeration


## -description


Defines the level of access that a handle has on files. 


## -enum-fields




### -field HAO_NONE

None.


### -field HAO_READ_ATTRIBUTES

The handle can be used to read file attributes.


### -field HAO_READ

The handle can be used to read the file.


### -field HAO_WRITE

The handle can be used to write to the file.


### -field HAO_DELETE

The handle can be used to delete the file.

