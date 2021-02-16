---
UID: NF:winsync.ISyncKnowledge.FindClockVectorForItem
title: ISyncKnowledge::FindClockVectorForItem (winsync.h)
description: Gets the clock vector that is associated with the specified item ID.
helpviewer_keywords: ["FindClockVectorForItem","FindClockVectorForItem method [Windows Sync]","FindClockVectorForItem method [Windows Sync]","ISyncKnowledge interface","ISyncKnowledge interface [Windows Sync]","FindClockVectorForItem method","ISyncKnowledge.FindClockVectorForItem","ISyncKnowledge::FindClockVectorForItem","winsync.isyncknowledge_findclockvectorforitem","winsync/ISyncKnowledge::FindClockVectorForItem"]
old-location: winsync\isyncknowledge_findclockvectorforitem.htm
tech.root: winsync
ms.assetid: d0df840c-c0ca-4fd8-b4bd-d4558e21b083
ms.date: 12/05/2018
ms.keywords: FindClockVectorForItem, FindClockVectorForItem method [Windows Sync], FindClockVectorForItem method [Windows Sync],ISyncKnowledge interface, ISyncKnowledge interface [Windows Sync],FindClockVectorForItem method, ISyncKnowledge.FindClockVectorForItem, ISyncKnowledge::FindClockVectorForItem, winsync.isyncknowledge_findclockvectorforitem, winsync/ISyncKnowledge::FindClockVectorForItem
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
 - ISyncKnowledge::FindClockVectorForItem
 - winsync/ISyncKnowledge::FindClockVectorForItem
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
 - ISyncKnowledge.FindClockVectorForItem
---

# ISyncKnowledge::FindClockVectorForItem


## -description

Gets the clock vector that is associated with the specified item ID.

## -parameters

### -param pbItemId [in]

The ID of the item that is associated with the clock vector to find.

### -param riid [in]

The IID of the object to retrieve. Must be <b>IID_IFeedClockVector</b> or <b>IID_IClockVector</b>.

### -param ppUnk [out]

Returns an object that implements <i>riid</i> and that represents the clock vector associated with <i>pbItemId</i>.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>