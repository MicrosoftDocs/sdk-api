---
UID: NF:winsync.ISyncCallback.OnChange
title: ISyncCallback::OnChange (winsync.h)
description: Occurs before a change is applied.
helpviewer_keywords: ["ISyncCallback interface [Windows Sync]","OnChange method","ISyncCallback.OnChange","ISyncCallback::OnChange","OnChange","OnChange method [Windows Sync]","OnChange method [Windows Sync]","ISyncCallback interface","winsync.isynccallback_onchange","winsync/ISyncCallback::OnChange"]
old-location: winsync\isynccallback_onchange.htm
tech.root: winsync
ms.assetid: 16bcc448-8acc-4349-a5d1-0c0764afe2ec
ms.date: 12/05/2018
ms.keywords: ISyncCallback interface [Windows Sync],OnChange method, ISyncCallback.OnChange, ISyncCallback::OnChange, OnChange, OnChange method [Windows Sync], OnChange method [Windows Sync],ISyncCallback interface, winsync.isynccallback_onchange, winsync/ISyncCallback::OnChange
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
 - ISyncCallback::OnChange
 - winsync/ISyncCallback::OnChange
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
 - ISyncCallback.OnChange
---

# ISyncCallback::OnChange


## -description

Occurs before a change is applied.

## -parameters

### -param pSyncChange [in]

The item change that is about to be applied.

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
<dt><b>Application-determined error codes.</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isynccallback">ISyncCallback Interface</a>