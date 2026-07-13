---
UID: NF:dpa_dsa.DPA_Search
title: DPA_Search function (dpa_dsa.h)
description: Finds an item in a dynamic pointer array (DPA).
helpviewer_keywords: ["DPAS_INSERTAFTER","DPAS_INSERTBEFORE","DPAS_SORTED","DPA_Search","DPA_Search function [Windows Controls]","_win32_DPA_Search","_win32_DPA_Search_cpp","controls.DPA_Search","controls._win32_DPA_Search","dpa_dsa/DPA_Search"]
old-location: controls\DPA_Search.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_search.htm
ms.date: 12/05/2018
ms.keywords: DPAS_INSERTAFTER, DPAS_INSERTBEFORE, DPAS_SORTED, DPA_Search, DPA_Search function [Windows Controls], _win32_DPA_Search, _win32_DPA_Search_cpp, controls.DPA_Search, controls._win32_DPA_Search, dpa_dsa/DPA_Search
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DPA_Search
 - dpa_dsa/DPA_Search
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComCtl32.dll
api_name:
 - DPA_Search
req.apiset: ext-ms-win-shell-comctl32-da-l1-1-0 (introduced in Windows 10, version 10.0.14393)
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

Type: <b><a href="/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndacompare">PFNDPACOMPARE</a></b>

A comparison function pointer. See <a href="/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndacompare">PFNDPACOMPARE</a> for the comparison function prototype.

### -param lParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

An additional parameter to be passed to <i>pfnCmp</i>.

### -param options

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

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
