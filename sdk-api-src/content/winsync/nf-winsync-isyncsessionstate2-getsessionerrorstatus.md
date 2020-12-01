---
UID: NF:winsync.ISyncSessionState2.GetSessionErrorStatus
title: ISyncSessionState2::GetSessionErrorStatus (winsync.h)
description: Gets the error value that indicates why the synchronization session failed.
helpviewer_keywords: ["GetSessionErrorStatus","GetSessionErrorStatus method [Windows Sync]","GetSessionErrorStatus method [Windows Sync]","ISyncSessionState2 interface","ISyncSessionState2 interface [Windows Sync]","GetSessionErrorStatus method","ISyncSessionState2.GetSessionErrorStatus","ISyncSessionState2::GetSessionErrorStatus","winsync.isyncsessionstate2_getsessionerrorstatus","winsync/ISyncSessionState2::GetSessionErrorStatus"]
old-location: winsync\isyncsessionstate2_getsessionerrorstatus.htm
tech.root: winsync
ms.assetid: 74b263c0-ef6a-4159-9ea2-301b7064331d
ms.date: 12/05/2018
ms.keywords: GetSessionErrorStatus, GetSessionErrorStatus method [Windows Sync], GetSessionErrorStatus method [Windows Sync],ISyncSessionState2 interface, ISyncSessionState2 interface [Windows Sync],GetSessionErrorStatus method, ISyncSessionState2.GetSessionErrorStatus, ISyncSessionState2::GetSessionErrorStatus, winsync.isyncsessionstate2_getsessionerrorstatus, winsync/ISyncSessionState2::GetSessionErrorStatus
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
 - ISyncSessionState2::GetSessionErrorStatus
 - winsync/ISyncSessionState2::GetSessionErrorStatus
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
 - ISyncSessionState2.GetSessionErrorStatus
---

# ISyncSessionState2::GetSessionErrorStatus


## -description

Gets the error value that indicates why the synchronization session failed.

## -parameters

### -param phrSessionError [out]

The error value that indicates why the synchronization session failed.

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
<dt><b>E_POINTER
</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncsessionstate">ISyncSessionState Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncsessionstate2">ISyncSessionState2 Interface</a>