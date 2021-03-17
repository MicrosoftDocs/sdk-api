---
UID: NF:winsync.ICoreFragment.GetColumnCount
title: ICoreFragment::GetColumnCount (winsync.h)
description: Gets the number of columns that are contained in this knowledge fragment.
helpviewer_keywords: ["GetColumnCount","GetColumnCount method [Windows Sync]","GetColumnCount method [Windows Sync]","ICoreFragment interface","ICoreFragment interface [Windows Sync]","GetColumnCount method","ICoreFragment.GetColumnCount","ICoreFragment::GetColumnCount","winsync.icorefragment_getcolumncount","winsync/ICoreFragment::GetColumnCount"]
old-location: winsync\icorefragment_getcolumncount.htm
tech.root: winsync
ms.assetid: 5f1aff6d-4fdf-48e1-9c7b-c003ec27f354
ms.date: 12/05/2018
ms.keywords: GetColumnCount, GetColumnCount method [Windows Sync], GetColumnCount method [Windows Sync],ICoreFragment interface, ICoreFragment interface [Windows Sync],GetColumnCount method, ICoreFragment.GetColumnCount, ICoreFragment::GetColumnCount, winsync.icorefragment_getcolumncount, winsync/ICoreFragment::GetColumnCount
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
 - ICoreFragment::GetColumnCount
 - winsync/ICoreFragment::GetColumnCount
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
 - ICoreFragment.GetColumnCount
---

# ICoreFragment::GetColumnCount


## -description

Gets the number of columns that are contained in this knowledge fragment.

## -parameters

### -param pColumnCount [out]

Returns the number of columns that are contained in this knowledge fragment.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>

## -remarks

An <b>ISyncKnowledge2</b> object contains one or more <b>ICoreFragment</b> objects. Each object contains knowledge that applies to a specific set of columns. A column is represented as a change unit. Typically, one of the <b>ICoreFragment</b> objects contains no columns. When an <b>ICoreFragment</b> object contains no columns, its knowledge applies to all of the change units that are not specified in any other fragment.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-icorefragment">ICoreFragment Interface</a>