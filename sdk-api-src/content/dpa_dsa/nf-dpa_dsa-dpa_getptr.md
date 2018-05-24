---
UID: NF:dpa_dsa.DPA_GetPtr
title: DPA_GetPtr function
author: windows-driver-content
description: Gets an item from a dynamic pointer array (DPA).
old-location: controls\DPA_GetPtr.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_getptr.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: DPA_GetPtr, DPA_GetPtr function [Windows Controls], _win32_DPA_GetPtr, _win32_DPA_GetPtr_cpp, controls.DPA_GetPtr, controls._win32_DPA_GetPtr, dpa_dsa/DPA_GetPtr
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
req.typenames: CRYPTPROTECT_PROMPTSTRUCT, *PCRYPTPROTECT_PROMPTSTRUCT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	ComCtl32.dll
api_name:
-	DPA_GetPtr
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: ComCtl32.dll
req.irql: 
---

# DPA_GetPtr function


## -description


<p class="CCE_Message">[<b>DPA_GetPtr</b> is available for use in the operating 

systems specified in the Requirements section. It may be altered or unavailable in 

subsequent versions.]

Gets an item from a dynamic pointer array (DPA).


## -parameters




### -param hdpa

TBD


### -param i

TBD




#### - index

Type: <b>int</b>

The index of item to be retrieved.


#### - pdpa

Type: <b>HDPA</b>

A handle to a DPA.


## -returns



Returns the specified item or <b>NULL</b>, if the call fails.



