---
UID: NF:winsync.ICoreFragment.NextColumn
title: ICoreFragment::NextColumn (winsync.h)
description: Returns the next change unit ID in the set of change unit IDs that this knowledge fragment applies to.
helpviewer_keywords: ["ICoreFragment interface [Windows Sync]","NextColumn method","ICoreFragment.NextColumn","ICoreFragment::NextColumn","NextColumn","NextColumn method [Windows Sync]","NextColumn method [Windows Sync]","ICoreFragment interface","winsync.icorefragment_nextcolumn","winsync/ICoreFragment::NextColumn"]
old-location: winsync\icorefragment_nextcolumn.htm
tech.root: winsync
ms.assetid: d50527cb-00ba-4e7b-9fb3-267eaa6cd6e6
ms.date: 12/05/2018
ms.keywords: ICoreFragment interface [Windows Sync],NextColumn method, ICoreFragment.NextColumn, ICoreFragment::NextColumn, NextColumn, NextColumn method [Windows Sync], NextColumn method [Windows Sync],ICoreFragment interface, winsync.icorefragment_nextcolumn, winsync/ICoreFragment::NextColumn
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - ICoreFragment::NextColumn
 - winsync/ICoreFragment::NextColumn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ICoreFragment.NextColumn
---

# ICoreFragment::NextColumn


## -description

Returns the next change unit ID in the set of change unit IDs that this knowledge fragment applies to.

## -parameters

### -param pChangeUnitId [in, out]

Returns the next change unit ID in the set.

### -param pChangeUnitIdSize [in, out]

Specifies the number of bytes in <i>pChangeUnitId</i>. Returns the number of bytes written, or the number of bytes that are required to retrieve the ID when <i>pChangeUnitId</i> is too small.

## -returns

The possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There are no more change unit IDs to enumerate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The change unit ID is a variable-length ID and <i>pChangeUnitIdSize</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_MORE_DATA)</b></dt>
</dl>
</td>
<td width="60%">
<i>pChangeUnitId</i> is too small. In this situation, the required number of bytes is returned in <i>pChangeUnitIdSize</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The knowledge object contained within this object has changed since this object was created.

</td>
</tr>
</table>

## -remarks

An <b>ISyncKnowledge2</b> object contains one or more <b>ICoreFragment</b> objects, each of which contains knowledge that applies to a specific set of columns. Typically, one of the <b>ICoreFragment</b> objects contains no columns, and its knowledge applies to all of the change units that are not specified in any other fragment. In this situation, <b>NextColumn</b> always returns <b>S_FALSE</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-icorefragment">ICoreFragment Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge2 Interface</a>