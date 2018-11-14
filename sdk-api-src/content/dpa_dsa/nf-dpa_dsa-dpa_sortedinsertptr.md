---
UID: NF:dpa_dsa.DPA_SortedInsertPtr
title: DPA_SortedInsertPtr macro
author: windows-sdk-content
description: Inserts a new item before or after a specified existing item.
old-location: controls\DPA_SortedInsertPtr.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\common\macros\dpa_sortedinsertptr.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DPAS_INSERTAFTER, DPAS_INSERTBEFORE, DPA_SortedInsertPtr, DPA_SortedInsertPtr macro [Windows Controls], _shell_DPA_SortedInsertPtr, _shell_DPA_SortedInsertPtr_cpp, controls.DPA_SortedInsertPtr, controls._shell_DPA_SortedInsertPtr, dpa_dsa/DPA_SortedInsertPtr
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dpa_dsa.h
api_name:
 - DPA_SortedInsertPtr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- dpa_dsa.h
: 
- DPA_SortedInsertPtr
: 
---

# DPA_SortedInsertPtr macro


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

Type: <b><a href="https://msdn.microsoft.com/b2b03db5-e595-4778-b51a-0087d663b026">PFNDPACOMPARE</a></b>

A pointer to the comparison function. See <a href="https://msdn.microsoft.com/b2b03db5-e595-4778-b51a-0087d663b026">PFNDPACOMPARE</a> or <a href="https://msdn.microsoft.com/49e2b929-155d-447b-8935-7fe2a128874e">PFNDPACOMPARECONST</a> for the comparison function prototype.


### -param lParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

An additional parameter used to pass information to the comparison function pointed to by <i>pfnCmp</i>.


### -param options

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

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



<div class="alert"><b>Note</b>  This macro wraps the <a href="https://msdn.microsoft.com/en-us/library/Bb775625(v=VS.85).aspx">DPA_InsertPtr</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb775633(v=VS.85).aspx">DPA_Search</a> functions.</div>
<div> </div>
The DPAS_SORTED flag is included in <i>options</i> by default to indicate that the DPA is sorted.

See function <a href="https://msdn.microsoft.com/en-us/library/Bb775633(v=VS.85).aspx">DPA_Search</a> for additional information on how the <i>pFind</i> item is located. The new item is inserted before or after the <i>pFind</i> item according to the <i>options</i> parameter. The <i>pFind</i> parameter need not exist in the DPA. If it does not exist in the DPA, then the new item is inserted where <i>pFind</i> would have been had it been inserted in the DPA in sorted order.



