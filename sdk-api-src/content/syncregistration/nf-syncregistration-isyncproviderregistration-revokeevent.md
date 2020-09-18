---
UID: NF:syncregistration.ISyncProviderRegistration.RevokeEvent
title: ISyncProviderRegistration::RevokeEvent (syncregistration.h)
description: Unregisters the user from the notification of the arrival of new registration events.
helpviewer_keywords: ["ISyncProviderRegistration interface [Windows Sync]","RevokeEvent method","ISyncProviderRegistration.RevokeEvent","ISyncProviderRegistration::RevokeEvent","RevokeEvent","RevokeEvent method [Windows Sync]","RevokeEvent method [Windows Sync]","ISyncProviderRegistration interface","syncregistration/ISyncProviderRegistration::RevokeEvent","winsync.isyncproviderregistration_revokeevent"]
old-location: winsync\isyncproviderregistration_revokeevent.htm
tech.root: winsync
ms.assetid: fcc4901a-1507-461e-bbcc-a9e440ec05ce
ms.date: 12/05/2018
ms.keywords: ISyncProviderRegistration interface [Windows Sync],RevokeEvent method, ISyncProviderRegistration.RevokeEvent, ISyncProviderRegistration::RevokeEvent, RevokeEvent, RevokeEvent method [Windows Sync], RevokeEvent method [Windows Sync],ISyncProviderRegistration interface, syncregistration/ISyncProviderRegistration::RevokeEvent, winsync.isyncproviderregistration_revokeevent
req.header: syncregistration.h
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
 - ISyncProviderRegistration::RevokeEvent
 - syncregistration/ISyncProviderRegistration::RevokeEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncregistration.h
api_name:
 - ISyncProviderRegistration.RevokeEvent
---

# ISyncProviderRegistration::RevokeEvent


## -description

Unregisters the user from the notification of the arrival of new registration
		events.

## -parameters

### -param hEvent [in]

The <b>HANDLE</b> returned by the <a href="/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderregistration-registerforevent">RegisterForEvent</a> method.

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
<td width="60%">
The specified event has not been registered.

</td>
</tr>
</table>

## -remarks

This method closes the specified <b>HANDLE</b> and cleans up any related memory.

## -see-also

<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderregistration">ISyncProviderRegistration Interface</a>