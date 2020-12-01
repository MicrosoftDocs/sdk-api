---
UID: NF:syncregistration.ISyncRegistrationChange.GetInstanceId
title: ISyncRegistrationChange::GetInstanceId (syncregistration.h)
description: Gets the instance ID of the synchronization provider or synchronization provider configuration UI associated with the event.
helpviewer_keywords: ["GetInstanceId","GetInstanceId method [Windows Sync]","GetInstanceId method [Windows Sync]","ISyncRegistrationChange interface","ISyncRegistrationChange interface [Windows Sync]","GetInstanceId method","ISyncRegistrationChange.GetInstanceId","ISyncRegistrationChange::GetInstanceId","syncregistration/ISyncRegistrationChange::GetInstanceId","winsync.isyncregistrationchange_getinstanceid"]
old-location: winsync\isyncregistrationchange_getinstanceid.htm
tech.root: winsync
ms.assetid: 2b2655f4-2a67-405d-93dc-dd8242992ce5
ms.date: 12/05/2018
ms.keywords: GetInstanceId, GetInstanceId method [Windows Sync], GetInstanceId method [Windows Sync],ISyncRegistrationChange interface, ISyncRegistrationChange interface [Windows Sync],GetInstanceId method, ISyncRegistrationChange.GetInstanceId, ISyncRegistrationChange::GetInstanceId, syncregistration/ISyncRegistrationChange::GetInstanceId, winsync.isyncregistrationchange_getinstanceid
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
 - ISyncRegistrationChange::GetInstanceId
 - syncregistration/ISyncRegistrationChange::GetInstanceId
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
 - ISyncRegistrationChange.GetInstanceId
---

# ISyncRegistrationChange::GetInstanceId


## -description

Gets the instance ID of the synchronization provider or synchronization provider configuration UI associated with the event.

## -parameters

### -param pguidInstanceId [out]

The instance ID.

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