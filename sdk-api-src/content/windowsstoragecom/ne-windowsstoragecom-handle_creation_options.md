---
UID: NE:windowsstoragecom.HANDLE_CREATION_OPTIONS
title: HANDLE_CREATION_OPTIONS
author: windows-sdk-content
description: Represents the action to take on a file that exists or doesn't exist.
old-location: winrt\handle_creation_options.htm
tech.root: WinRT
ms.assetid: 94EE8D50-A85C-4AA2-9A8A-A382AD308B7B
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: HANDLE_CREATION_OPTIONS, HANDLE_CREATION_OPTIONS enumeration [Windows Runtime], HCO_CREATE_ALWAYS, HCO_CREATE_NEW, HCO_OPEN_ALWAYS, HCO_OPEN_EXISTING, HCO_TRUNCATE_EXISTING, windowsstoragecom/HANDLE_CREATION_OPTIONS, windowsstoragecom/HCO_CREATE_ALWAYS, windowsstoragecom/HCO_CREATE_NEW, windowsstoragecom/HCO_OPEN_ALWAYS, windowsstoragecom/HCO_OPEN_EXISTING, windowsstoragecom/HCO_TRUNCATE_EXISTING, winrt.handle_creation_options
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - windowsstoragecom.h
api_name:
 - HANDLE_CREATION_OPTIONS
product: Windows
targetos: Windows
req.typenames: HANDLE_CREATION_OPTIONS
req.redist: 
---

# HANDLE_CREATION_OPTIONS enumeration


## -description


Represents the action to take on a file that exists or doesn't exist. 


## -enum-fields




### -field HCO_CREATE_NEW

Create a new file, only if it doesn't already exist.



### -field HCO_CREATE_ALWAYS

Create a new file, always.



### -field HCO_OPEN_EXISTING

Open a file only if it exists.


### -field HCO_OPEN_ALWAYS

Open a file, always.


### -field HCO_TRUNCATE_EXISTING

Open a file and truncates it so that its size is zero bytes, only if it exists.


