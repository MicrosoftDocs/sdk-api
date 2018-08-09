---
UID: NF:shobjidl_core.FreeIDListArrayFull
title: FreeIDListArrayFull function
author: windows-sdk-content
description: Releases the memory space for the pointer to an item identifier list (PIDL) array. This releases both the PIDLIST_ABSOLUTEs within the array and the array itself.
old-location: shell\FreeIDListArrayFull.htm
old-project: shell
ms.assetid: ca5e9e02-dcab-4aac-953e-8be0ca8734bc
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FreeIDListArrayFull, FreeIDListArrayFull function [Windows Shell], _shell_FreeIDListArrayFull, shell.FreeIDListArrayFull, shobjidl_core/FreeIDListArrayFull
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - FreeIDListArrayFull
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# FreeIDListArrayFull function


## -description


Releases the memory space for the pointer to an item identifier list (PIDL) array. This releases both the PIDLIST_ABSOLUTEs within the array and the array itself.


## -parameters




### -param ppidls [in]

Type: <b>PIDLIST_ABSOLUTE*</b>

A pointer to the PIDL list, stored as an array of <i>cItems</i> elements.


### -param cItems

Type: <b>UINT</b>

The number of items in the array.


## -returns



This function does not return a value.



