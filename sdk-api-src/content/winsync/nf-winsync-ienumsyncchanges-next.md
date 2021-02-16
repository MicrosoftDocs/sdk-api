---
UID: NF:winsync.IEnumSyncChanges.Next
title: IEnumSyncChanges::Next (winsync.h)
description: Returns the next item change.
helpviewer_keywords: ["IEnumSyncChanges interface [Windows Sync]","Next method","IEnumSyncChanges.Next","IEnumSyncChanges::Next","Next","Next method [Windows Sync]","Next method [Windows Sync]","IEnumSyncChanges interface","winsync.ienumsyncchanges_next","winsync/IEnumSyncChanges::Next"]
old-location: winsync\ienumsyncchanges_next.htm
tech.root: winsync
ms.assetid: 23b5f46f-87f3-431e-a253-d349eed27082
ms.date: 12/05/2018
ms.keywords: IEnumSyncChanges interface [Windows Sync],Next method, IEnumSyncChanges.Next, IEnumSyncChanges::Next, Next, Next method [Windows Sync], Next method [Windows Sync],IEnumSyncChanges interface, winsync.ienumsyncchanges_next, winsync/IEnumSyncChanges::Next
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
 - IEnumSyncChanges::Next
 - winsync/IEnumSyncChanges::Next
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
 - IEnumSyncChanges.Next
---

# IEnumSyncChanges::Next


## -description

Returns the next item change.

## -parameters

### -param cChanges [in]

The number of changes to fetch. The only valid value is 1.

### -param ppChange [out]

Returns the next item change.

### -param pcFetched [in, out]

Returns the number of changes that are fetched.

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
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ienumsyncchanges">IEnumSyncChanges Interface</a>