---
UID: NF:dpa_dsa.DPA_Sort
title: DPA_Sort function
author: windows-sdk-content
description: Sorts the items in a Dynamic Pointer Array (DPA).
old-location: controls\DPA_Sort.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_sort.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DPA_Sort, DPA_Sort function [Windows Controls], _win32_DPA_Sort, _win32_DPA_Sort_cpp, controls.DPA_Sort, controls._win32_DPA_Sort, dpa_dsa/DPA_Sort
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
 - DPA_Sort
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: ComCtl32.dll
req.irql: 
---

# DPA_Sort function


## -description


<p class="CCE_Message">[<b>DPA_Sort</b> is available for use in the operating 

systems specified in the Requirements section. It may be altered or unavailable in 

subsequent versions.]

Sorts the items in a Dynamic Pointer Array (DPA).


## -parameters




### -param hdpa

Type: <b>HDPA</b>

A handle to a DPA.


### -param pfnCompare

Type: <b><a href="https://msdn.microsoft.com/b2b03db5-e595-4778-b51a-0087d663b026">PFNDPACOMPARE</a></b>

A comparison function pointer. See <a href="https://msdn.microsoft.com/b2b03db5-e595-4778-b51a-0087d663b026">PFNDPACOMPARE</a> for the comparison function prototype.


### -param lParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

An additional parameter to be passed to <i>pfnCmp</i>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns <b>TRUE</b> on success or <b>FALSE</b> on failure.



