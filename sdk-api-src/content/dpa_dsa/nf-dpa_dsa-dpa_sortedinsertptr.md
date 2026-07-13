---
UID: NF:dpa_dsa.DPA_SortedInsertPtr
title: DPA_SortedInsertPtr macro (dpa_dsa.h)
description: Inserts a new item before or after a specified existing item.
helpviewer_keywords: ["DPAS_INSERTAFTER","DPAS_INSERTBEFORE","DPA_SortedInsertPtr","DPA_SortedInsertPtr macro [Windows Controls]","_shell_DPA_SortedInsertPtr","_shell_DPA_SortedInsertPtr_cpp","controls.DPA_SortedInsertPtr","controls._shell_DPA_SortedInsertPtr","dpa_dsa/DPA_SortedInsertPtr"]
old-location: controls\DPA_SortedInsertPtr.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\macros\dpa_sortedinsertptr.htm
ms.date: 10/21/2024
ms.keywords: DPAS_INSERTAFTER, DPAS_INSERTBEFORE, DPA_SortedInsertPtr, DPA_SortedInsertPtr macro [Windows Controls], _shell_DPA_SortedInsertPtr, _shell_DPA_SortedInsertPtr_cpp, controls.DPA_SortedInsertPtr, controls._shell_DPA_SortedInsertPtr, dpa_dsa/DPA_SortedInsertPtr
req.header: dpa_dsa.h
req.include-header: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DPA_SortedInsertPtr
 - dpa_dsa/DPA_SortedInsertPtr
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dpa_dsa.h
api_name:
 - DPA_SortedInsertPtr
---

# DPA_SortedInsertPtr macro

## -syntax

```cpp
int DPA_SortedInsertPtr(
   HDPA          hdpa,
   void          *pFind,
   int           iStart,
   PFNDPACOMPARE pfnCompare,
   LPARAM        lParam,
   UINT          options,
   void          *pitem
);
```

## -returns

Type: **int**

Returns the index of the new item, or <code>-1</code> if the insert action fails.

## -description

Inserts a new item before or after a specified existing item.

## -parameters

### -param hdpa

Type: <b>HDPA</b>

A handle to a DPA.

### -param pFind

Type: <b>void*</b>

An item pointer which is used to determine the insertion point for the new item (see Remarks).

### -param iStart

Type: <b>int</b>

The index in the DPA at which to begin searching for <i>pFind</i>.

### -param pfnCompare

Type: <b><a href="/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndacompare">PFNDPACOMPARE</a></b>

A pointer to the comparison function. See <a href="/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndacompare">PFNDPACOMPARE</a> or <a href="/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndacompareconst">PFNDPACOMPARECONST</a> for the comparison function prototype.

### -param lParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

An additional parameter used to pass information to the comparison function pointed to by <i>pfnCompare</i>.

### -param options

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The insertion point. Must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DPAS_INSERTBEFORE"></a><a id="dpas_insertbefore"></a><dl>
<dt><b>DPAS_INSERTBEFORE</b></dt>
</dl>
</td>
<td width="60%">
Insert the new item before the <i>pFind</i> item.

</td>
</tr>
<tr>
<td width="40%"><a id="DPAS_INSERTAFTER"></a><a id="dpas_insertafter"></a><dl>
<dt><b>DPAS_INSERTAFTER</b></dt>
</dl>
</td>
<td width="60%">
Insert the new item after the <i>pFind</i> item.

</td>
</tr>
</table>

### -param pitem

Type: <b>void*</b>

A pointer to the item that is to be inserted.

## -remarks

<div class="alert"><b>Note</b>  This macro wraps the <a href="/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_insertptr">DPA_InsertPtr</a> and <a href="/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_search">DPA_Search</a> functions.</div>
<div> </div>
The DPAS_SORTED flag is included in <i>options</i> by default to indicate that the DPA is sorted.

See function <a href="/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_search">DPA_Search</a> for additional information on how the <i>pFind</i> item is located. The new item is inserted before or after the <i>pFind</i> item according to the <i>options</i> parameter. The <i>pFind</i> parameter need not exist in the DPA. If it does not exist in the DPA, then the new item is inserted where <i>pFind</i> would have been had it been inserted in the DPA in sorted order.
