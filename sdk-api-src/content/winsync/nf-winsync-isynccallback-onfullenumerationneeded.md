---
UID: NF:winsync.ISyncCallback.OnFullEnumerationNeeded
title: ISyncCallback::OnFullEnumerationNeeded (winsync.h)
description: Occurs when the forgotten knowledge from the source provider is not contained in the current knowledge of the destination provider.
helpviewer_keywords: ["ISyncCallback interface [Windows Sync]","OnFullEnumerationNeeded method","ISyncCallback.OnFullEnumerationNeeded","ISyncCallback::OnFullEnumerationNeeded","OnFullEnumerationNeeded","OnFullEnumerationNeeded method [Windows Sync]","OnFullEnumerationNeeded method [Windows Sync]","ISyncCallback interface","winsync.isynccallback_onfullenumerationneeded","winsync/ISyncCallback::OnFullEnumerationNeeded"]
old-location: winsync\isynccallback_onfullenumerationneeded.htm
tech.root: winsync
ms.assetid: f52ddaf2-9ce2-4ebb-bace-024c059b2594
ms.date: 12/05/2018
ms.keywords: ISyncCallback interface [Windows Sync],OnFullEnumerationNeeded method, ISyncCallback.OnFullEnumerationNeeded, ISyncCallback::OnFullEnumerationNeeded, OnFullEnumerationNeeded, OnFullEnumerationNeeded method [Windows Sync], OnFullEnumerationNeeded method [Windows Sync],ISyncCallback interface, winsync.isynccallback_onfullenumerationneeded, winsync/ISyncCallback::OnFullEnumerationNeeded
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
 - ISyncCallback::OnFullEnumerationNeeded
 - winsync/ISyncCallback::OnFullEnumerationNeeded
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
 - ISyncCallback.OnFullEnumerationNeeded
---

# ISyncCallback::OnFullEnumerationNeeded


## -description

Occurs when the forgotten knowledge from the source provider is not contained in the current knowledge of the destination provider.

## -parameters

### -param pFullEnumerationAction [out]

Specifies how a synchronization session should handle the full enumeration.

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

## -remarks

By default, if an application callback is not registered to receive this notification, Windows Sync uses <b>SFEA_ABORT</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isynccallback">ISyncCallback Interface</a>



<a href="/windows/win32/api/winsync/ne-winsync-sync_full_enumeration_action">SYNC_FULL_ENUMERATION_ACTION Enumeration</a>