---
UID: NE:windowsstoragecom.HANDLE_CREATION_OPTIONS
title: HANDLE_CREATION_OPTIONS (windowsstoragecom.h)
description: Represents the action to take on a file that exists or doesn't exist.
helpviewer_keywords: ["HANDLE_CREATION_OPTIONS","HANDLE_CREATION_OPTIONS enumeration [Windows Runtime]","HCO_CREATE_ALWAYS","HCO_CREATE_NEW","HCO_OPEN_ALWAYS","HCO_OPEN_EXISTING","HCO_TRUNCATE_EXISTING","windowsstoragecom/HANDLE_CREATION_OPTIONS","windowsstoragecom/HCO_CREATE_ALWAYS","windowsstoragecom/HCO_CREATE_NEW","windowsstoragecom/HCO_OPEN_ALWAYS","windowsstoragecom/HCO_OPEN_EXISTING","windowsstoragecom/HCO_TRUNCATE_EXISTING","winrt.handle_creation_options"]
old-location: winrt\handle_creation_options.htm
tech.root: WinRT
ms.assetid: 94EE8D50-A85C-4AA2-9A8A-A382AD308B7B
ms.date: 12/05/2018
ms.keywords: HANDLE_CREATION_OPTIONS, HANDLE_CREATION_OPTIONS enumeration [Windows Runtime], HCO_CREATE_ALWAYS, HCO_CREATE_NEW, HCO_OPEN_ALWAYS, HCO_OPEN_EXISTING, HCO_TRUNCATE_EXISTING, windowsstoragecom/HANDLE_CREATION_OPTIONS, windowsstoragecom/HCO_CREATE_ALWAYS, windowsstoragecom/HCO_CREATE_NEW, windowsstoragecom/HCO_OPEN_ALWAYS, windowsstoragecom/HCO_OPEN_EXISTING, windowsstoragecom/HCO_TRUNCATE_EXISTING, winrt.handle_creation_options
req.header: windowsstoragecom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
targetos: Windows
req.typenames: HANDLE_CREATION_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HANDLE_CREATION_OPTIONS
 - windowsstoragecom/HANDLE_CREATION_OPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - windowsstoragecom.h
api_name:
 - HANDLE_CREATION_OPTIONS
---

# HANDLE_CREATION_OPTIONS enumeration


## -description

Represents the action to take on a file that exists or doesn't exist.

## -enum-fields

### -field HCO_CREATE_NEW:0x1

Create a new file, only if it doesn't already exist.

### -field HCO_CREATE_ALWAYS:0x2

Create a new file, always.

### -field HCO_OPEN_EXISTING:0x3

Open a file only if it exists.

### -field HCO_OPEN_ALWAYS:0x4

Open a file, always.

### -field HCO_TRUNCATE_EXISTING:0x5

Open a file and truncates it so that its size is zero bytes, only if it exists.

