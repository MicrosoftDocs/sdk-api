---
UID: NF:winsync.ISyncChangeBatchAdvanced.GetUpperBoundItemId
title: ISyncChangeBatchAdvanced::GetUpperBoundItemId (winsync.h)
description: Gets the highest item ID that is represented in the knowledge of any group in the change batch.
helpviewer_keywords: ["GetUpperBoundItemId","GetUpperBoundItemId method [Windows Sync]","GetUpperBoundItemId method [Windows Sync]","ISyncChangeBatchAdvanced interface","ISyncChangeBatchAdvanced interface [Windows Sync]","GetUpperBoundItemId method","ISyncChangeBatchAdvanced.GetUpperBoundItemId","ISyncChangeBatchAdvanced::GetUpperBoundItemId","winsync.isyncchangebatchadvanced_getupperbounditemid","winsync/ISyncChangeBatchAdvanced::GetUpperBoundItemId"]
old-location: winsync\isyncchangebatchadvanced_getupperbounditemid.htm
tech.root: winsync
ms.assetid: 4aa472b1-7dfb-4159-8f50-cc8e5de34dd3
ms.date: 12/05/2018
ms.keywords: GetUpperBoundItemId, GetUpperBoundItemId method [Windows Sync], GetUpperBoundItemId method [Windows Sync],ISyncChangeBatchAdvanced interface, ISyncChangeBatchAdvanced interface [Windows Sync],GetUpperBoundItemId method, ISyncChangeBatchAdvanced.GetUpperBoundItemId, ISyncChangeBatchAdvanced::GetUpperBoundItemId, winsync.isyncchangebatchadvanced_getupperbounditemid, winsync/ISyncChangeBatchAdvanced::GetUpperBoundItemId
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
 - ISyncChangeBatchAdvanced::GetUpperBoundItemId
 - winsync/ISyncChangeBatchAdvanced::GetUpperBoundItemId
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
 - ISyncChangeBatchAdvanced.GetUpperBoundItemId
---

# ISyncChangeBatchAdvanced::GetUpperBoundItemId


## -description

Gets the highest item ID that is represented in the knowledge of any group in the change batch.

## -parameters

### -param pbItemId [in, out]

Returns the highest item ID that is represented in the knowledge of any group in the change batch.

### -param pcbIdSize [in, out]

Specifies the number of bytes in <i>pbItemId</i>. Returns the number of bytes that are necessary to retrieve the ID when <i>pbItemId</i> is too small, or returns the number of bytes written.

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
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_MORE_DATA)</b></dt>
</dl>
</td>
<td width="60%">
When <i>pbItemId</i> is too small. In this situation, the required number of bytes is returned in <i>pcbIdSize</i>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchadvanced">ISyncChangeBatchAdvanced Interface</a>