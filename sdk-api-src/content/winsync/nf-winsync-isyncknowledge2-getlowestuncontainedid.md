---
UID: NF:winsync.ISyncKnowledge2.GetLowestUncontainedId
title: ISyncKnowledge2::GetLowestUncontainedId (winsync.h)
description: Returns the lowest item ID that is not contained in this knowledge and that is contained in the specified knowledge.
helpviewer_keywords: ["GetLowestUncontainedId","GetLowestUncontainedId method [Windows Sync]","GetLowestUncontainedId method [Windows Sync]","ISyncKnowledge2 interface","ISyncKnowledge2 interface [Windows Sync]","GetLowestUncontainedId method","ISyncKnowledge2.GetLowestUncontainedId","ISyncKnowledge2::GetLowestUncontainedId","winsync.isyncknowledge2_getlowestuncontainedid","winsync/ISyncKnowledge2::GetLowestUncontainedId"]
old-location: winsync\isyncknowledge2_getlowestuncontainedid.htm
tech.root: winsync
ms.assetid: 06a1a380-3fe8-4c99-be97-d84b6be9838d
ms.date: 12/05/2018
ms.keywords: GetLowestUncontainedId, GetLowestUncontainedId method [Windows Sync], GetLowestUncontainedId method [Windows Sync],ISyncKnowledge2 interface, ISyncKnowledge2 interface [Windows Sync],GetLowestUncontainedId method, ISyncKnowledge2.GetLowestUncontainedId, ISyncKnowledge2::GetLowestUncontainedId, winsync.isyncknowledge2_getlowestuncontainedid, winsync/ISyncKnowledge2::GetLowestUncontainedId
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
 - ISyncKnowledge2::GetLowestUncontainedId
 - winsync/ISyncKnowledge2::GetLowestUncontainedId
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
 - ISyncKnowledge2.GetLowestUncontainedId
---

# ISyncKnowledge2::GetLowestUncontainedId


## -description

Returns the lowest item ID that is not contained in this knowledge and that is contained in the specified knowledge.

## -parameters

### -param piSyncKnowledge [in]

The item ID that is returned in <i>pbItemId</i> is contained in <i>piSyncKnowledge</i>.

### -param pbItemId [in, out]

The lowest item ID that  is contained in <i>piSyncKnowledge</i> and is not contained in this knowledge.

### -param pcbItemIdSize [in, out]

The number of bytes in <i>pbItemId</i>. Returns either the number of bytes that are required to retrieve the ID when <i>pbItemId</i> is too small, or the number of bytes written.

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
<i>piSyncKnowledge</i> is contained in this knowledge. In this situation, there is no uncontained item ID to return.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The ID format schema of <i>piSyncKnowledge</i> is not the same as the ID format schema of this knowledge.

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
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_MORE_DATA)</b></dt>
</dl>
</td>
<td width="60%">
<i>pbItemId</i> is too small. In this situation, the required number of bytes is returned in <i>pcbItemIdSize</i>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge2">ISyncKnowledge2 Interface</a>