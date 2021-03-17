---
UID: NF:syncregistration.ISyncRegistrationChange.GetEvent
title: ISyncRegistrationChange::GetEvent (syncregistration.h)
description: Gets the next pending registration event.
helpviewer_keywords: ["GetEvent","GetEvent method [Windows Sync]","GetEvent method [Windows Sync]","ISyncRegistrationChange interface","ISyncRegistrationChange interface [Windows Sync]","GetEvent method","ISyncRegistrationChange.GetEvent","ISyncRegistrationChange::GetEvent","syncregistration/ISyncRegistrationChange::GetEvent","winsync.isyncregistrationchange_getevent"]
old-location: winsync\isyncregistrationchange_getevent.htm
tech.root: winsync
ms.assetid: 7c96c6ad-13ca-4e00-8e6e-61898206001f
ms.date: 12/05/2018
ms.keywords: GetEvent, GetEvent method [Windows Sync], GetEvent method [Windows Sync],ISyncRegistrationChange interface, ISyncRegistrationChange interface [Windows Sync],GetEvent method, ISyncRegistrationChange.GetEvent, ISyncRegistrationChange::GetEvent, syncregistration/ISyncRegistrationChange::GetEvent, winsync.isyncregistrationchange_getevent
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
 - ISyncRegistrationChange::GetEvent
 - syncregistration/ISyncRegistrationChange::GetEvent
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
 - ISyncRegistrationChange.GetEvent
---

# ISyncRegistrationChange::GetEvent


## -description

Gets the next pending registration event.

## -parameters

### -param psreEvent [out]

The registration event.

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

## -see-also

<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncregistrationchange">ISyncRegistrationChange Interface</a>