---
UID: NF:dpa_dsa.DPA_DeletePtr
title: DPA_DeletePtr function
author: windows-sdk-content
description: Removes an item from a dynamic pointer array (DPA). The DPA shrinks if necessary to accommodate the removed item.
old-location: controls\DPA_DeletePtr.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_deleteptr.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: DPA_DeletePtr, DPA_DeletePtr function [Windows Controls], _win32_DPA_DeletePtr, _win32_DPA_DeletePtr_cpp, controls.DPA_DeletePtr, controls._win32_DPA_DeletePtr, dpa_dsa/DPA_DeletePtr
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: CRYPTPROTECT_PROMPTSTRUCT, *PCRYPTPROTECT_PROMPTSTRUCT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComCtl32.dll
api_name:
 - DPA_DeletePtr
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: ComCtl32.dll
req.irql: 
---

# DPA_DeletePtr function


## -description


<p class="CCE_Message">[<b>DPA_DeletePtr</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Removes an item from a dynamic pointer array (DPA). The DPA shrinks if necessary to accommodate the removed item.


## -parameters




### -param hdpa

TBD


### -param i

TBD




#### - index

Type: <b>int</b>

An index of item to be removed from DPA.


#### - pdpa

Type: <b>HDPA</b>

A handle to a DPA.


## -returns



Returns the removed item or <b>NULL</b>, if the call fails.



