---
UID: NF:dpa_dsa.DPA_Search
title: DPA_Search function
author: windows-sdk-content
description: Finds an item in a dynamic pointer array (DPA).
old-location: controls\DPA_Search.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_search.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DPAS_INSERTAFTER, DPAS_INSERTBEFORE, DPAS_SORTED, DPA_Search, DPA_Search function [Windows Controls], _win32_DPA_Search, _win32_DPA_Search_cpp, controls.DPA_Search, controls._win32_DPA_Search, dpa_dsa/DPA_Search
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dpa_dsa.h
req.include-header: 
req.redist: 
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
 - DPA_Search
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: ComCtl32.dll
req.irql: 
---

# DPA_Search function


## -description


<p class="CCE_Message">[<b>DPA_Search</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Finds an item in a dynamic pointer array (DPA).


## -parameters




### -param hdpa

Type: <b>HDPA</b>

A handle to a DPA.


### -param pFind

Type: <b>void*</b>

A pointer to search for.


### -param iStart

Type: <b>int</b>

The index at which to start search.


### -param pfnCompare

Type: <b><a href="https://msdn.microsoft.com/b2b03db5-e595-4778-b51a-0087d663b026">PFNDPACOMPARE</a></b>

A comparison function pointer. See <a href="https://msdn.microsoft.com/b2b03db5-e595-4778-b51a-0087d663b026">PFNDPACOMPARE</a> for the comparison function prototype.


### -param lParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

An additional parameter to be passed to <i>pfnCmp</i>.


### -param options

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

This parameter may be one or more of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DPAS_SORTED"></a><a id="dpas_sorted"></a><dl>
<dt><b>DPAS_SORTED</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the DPA is sorted.

</td>
</tr>
<tr>
<td width="40%"><a id="DPAS_INSERTBEFORE"></a><a id="dpas_insertbefore"></a><dl>
<dt><b>DPAS_INSERTBEFORE</b></dt>
</dl>
</td>
<td width="60%">
This value is only valid in conjunction with DPAS_SORTED. If the item is not found, return the position where the item is expected to be found in the sorted DPA.

</td>
</tr>
<tr>
<td width="40%"><a id="DPAS_INSERTAFTER"></a><a id="dpas_insertafter"></a><dl>
<dt><b>DPAS_INSERTAFTER</b></dt>
</dl>
</td>
<td width="60%">
This value is only valid in conjunction with DPAS_SORTED. If the item is not found, return the position where the item is expected to be found in the sorted DPA.

</td>
</tr>
</table>
 


## -returns



Type: <b>int</b>

Returns the index where the item was found in the DPA or <code>-1</code> if the item was not found.



