---
UID: NF:dpa_dsa.DSA_InsertItem
title: DSA_InsertItem function
author: windows-sdk-content
description: Inserts a new item into a dynamic structure array (DSA). If necessary, the DSA expands to accommodate the new item.
old-location: controls\DSA_InsertItem.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\common\functions\dsa_insertitem.htm
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: DSA_InsertItem, DSA_InsertItem function [Windows Controls], _win32_DSA_InsertItem, _win32_DSA_InsertItem_cpp, controls.DSA_InsertItem, controls._win32_DSA_InsertItem, dpa_dsa/DSA_InsertItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dpa_dsa.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comctl32.lib
req.dll: ComCtl32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComCtl32.dll
api_name:
 - DSA_InsertItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DSA_InsertItem function


## -description


<p class="CCE_Message">[<b>DSA_InsertItem</b> is available for use in the operating 

systems specified in the Requirements section. It may be altered or unavailable in 

subsequent versions.]

Inserts a new item into a dynamic structure array (DSA). If necessary, the DSA expands to accommodate the new item.


## -parameters




### -param hdsa [in]

Type: <b>HDSA</b>

A handle to the DSA in which to insert the item.


### -param i [in]

Type: <b>int</b>

The position in the DSA where new item is to be inserted, or DSA_APPEND to insert the item at the end of the array.


### -param pitem [in]

Type: <b>void*</b>

A pointer to the item that is to be inserted.


## -returns



Type: <b>int</b>

Returns the index of the new item if the insertion succeeds, or DSA_ERR (<code>-1</code>) if the insertion fails.




## -remarks



The actual data pointed to by <i>pItem</i> is copied into the DSA. Subsequent actions performed on that item do not affect the original copy.



