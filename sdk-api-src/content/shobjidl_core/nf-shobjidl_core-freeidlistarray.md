---
UID: NF:shobjidl_core.FreeIDListArray
title: FreeIDListArray function
author: windows-sdk-content
description: Frees the memory used by an pointer to an item identifier list (PIDL) list array.
old-location: shell\FreeIDListArray.htm
old-project: shell
ms.assetid: 42496da6-452e-45cb-9061-74eba95aff7e
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: FreeIDListArray, FreeIDListArray function [Windows Shell], _shell_FreeIDListArray, shell.FreeIDListArray, shobjidl_core/FreeIDListArray
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
 - FreeIDListArray
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# FreeIDListArray function


## -description


Frees the memory used by an pointer to an item identifier list (PIDL) list array.


## -parameters




### -param ppidls [in]

Type: <b>PIDLIST_RELATIVE*</b>

A pointer to the list of <i>cItems</i> PIDLs, stored as an array.


### -param cItems

Type: <b>UINT</b>

The number of items in the array.


## -returns



This function does not return a value.



