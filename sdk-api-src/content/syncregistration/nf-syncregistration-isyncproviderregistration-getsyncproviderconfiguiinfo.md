---
UID: NF:syncregistration.ISyncProviderRegistration.GetSyncProviderConfigUIInfo
title: ISyncProviderRegistration::GetSyncProviderConfigUIInfo (syncregistration.h)
description: Returns an ISyncProviderConfigUIInfo object for the given unique instance ID.
helpviewer_keywords: ["GetSyncProviderConfigUIInfo","GetSyncProviderConfigUIInfo method [Windows Sync]","GetSyncProviderConfigUIInfo method [Windows Sync]","ISyncProviderRegistration interface","ISyncProviderRegistration interface [Windows Sync]","GetSyncProviderConfigUIInfo method","ISyncProviderRegistration.GetSyncProviderConfigUIInfo","ISyncProviderRegistration::GetSyncProviderConfigUIInfo","syncregistration/ISyncProviderRegistration::GetSyncProviderConfigUIInfo","winsync.isyncproviderregistration_getsyncproviderconfiguiinfo"]
old-location: winsync\isyncproviderregistration_getsyncproviderconfiguiinfo.htm
tech.root: winsync
ms.assetid: 687f2f28-378e-456c-a06a-d78e486e6635
ms.date: 12/05/2018
ms.keywords: GetSyncProviderConfigUIInfo, GetSyncProviderConfigUIInfo method [Windows Sync], GetSyncProviderConfigUIInfo method [Windows Sync],ISyncProviderRegistration interface, ISyncProviderRegistration interface [Windows Sync],GetSyncProviderConfigUIInfo method, ISyncProviderRegistration.GetSyncProviderConfigUIInfo, ISyncProviderRegistration::GetSyncProviderConfigUIInfo, syncregistration/ISyncProviderRegistration::GetSyncProviderConfigUIInfo, winsync.isyncproviderregistration_getsyncproviderconfiguiinfo
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
 - ISyncProviderRegistration::GetSyncProviderConfigUIInfo
 - syncregistration/ISyncProviderRegistration::GetSyncProviderConfigUIInfo
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
 - ISyncProviderRegistration.GetSyncProviderConfigUIInfo
---

# ISyncProviderRegistration::GetSyncProviderConfigUIInfo


## -description

Returns an <a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderconfiguiinfo">ISyncProviderConfigUIInfo</a> object for the given unique instance ID.

## -parameters

### -param pguidInstanceId [in]

The unique instance ID of the <b>ISyncProviderConfigUIInfo</b> object.

### -param ppConfigUIInfo [out]

The configuration UI information object.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough memory available to return the configuration UI.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_REGISTRATION_NOTREGISTERED  </b></dt>
</dl>
</td>
<td width="60%">
A configuration UI with the specified instance ID was not registered.

</td>
</tr>
</table>

## -remarks

This method is used to get and set the configuration UI properties for the specified  configuration UI object.

## -see-also

<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderconfiguiinfo">ISyncProviderConfigUIInfo Interface</a>



<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderregistration">ISyncProviderRegistration Interface</a>