---
UID: NF:shobjidl_core.FreeIDListArrayChild
title: FreeIDListArrayChild function
author: windows-sdk-content
description: Releases the memory space for the array of pointers to child item IDs. This releases both the PITEMID_CHILDs within the array and the array itself.
old-location: shell\FreeIDListArrayChild.htm
tech.root: shell
ms.assetid: 89abceae-1aed-401d-82ab-57215ec22d00
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: FreeIDListArrayChild, FreeIDListArrayChild function [Windows Shell], _shell_FreeIDListArrayChild, shell.FreeIDListArrayChild, shobjidl_core/FreeIDListArrayChild
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - FreeIDListArrayChild
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FreeIDListArrayChild function


## -description


Releases the memory space for the array of pointers to child item IDs. This releases both the PITEMID_CHILDs within the array and the array itself.


## -parameters




### -param ppidls [in]

Type: <b>PITEMID_CHILD*</b>

A pointer to the PIDL list, stored as an array of <i>cItems</i> elements.


### -param cItems

Type: <b>UINT</b>

The number of items in the array.


## -returns



This function does not return a value.



