---
UID: NF:syncregistration.ISyncProviderRegistration.GetSyncProviderConfigUIFromInstanceId
title: ISyncProviderRegistration::GetSyncProviderConfigUIFromInstanceId (syncregistration.h)
description: Returns an initialized and instantiated ISyncProviderConfigUI object for the given unique instance ID.
helpviewer_keywords: ["GetSyncProviderConfigUIFromInstanceId","GetSyncProviderConfigUIFromInstanceId method [Windows Sync]","GetSyncProviderConfigUIFromInstanceId method [Windows Sync]","ISyncProviderRegistration interface","ISyncProviderRegistration interface [Windows Sync]","GetSyncProviderConfigUIFromInstanceId method","ISyncProviderRegistration.GetSyncProviderConfigUIFromInstanceId","ISyncProviderRegistration::GetSyncProviderConfigUIFromInstanceId","syncregistration/ISyncProviderRegistration::GetSyncProviderConfigUIFromInstanceId","winsync.isyncproviderregistration_getsyncproviderconfiguifrominstanceid"]
old-location: winsync\isyncproviderregistration_getsyncproviderconfiguifrominstanceid.htm
tech.root: winsync
ms.assetid: 472732d7-39bd-434c-80f3-9808eca9035c
ms.date: 12/05/2018
ms.keywords: GetSyncProviderConfigUIFromInstanceId, GetSyncProviderConfigUIFromInstanceId method [Windows Sync], GetSyncProviderConfigUIFromInstanceId method [Windows Sync],ISyncProviderRegistration interface, ISyncProviderRegistration interface [Windows Sync],GetSyncProviderConfigUIFromInstanceId method, ISyncProviderRegistration.GetSyncProviderConfigUIFromInstanceId, ISyncProviderRegistration::GetSyncProviderConfigUIFromInstanceId, syncregistration/ISyncProviderRegistration::GetSyncProviderConfigUIFromInstanceId, winsync.isyncproviderregistration_getsyncproviderconfiguifrominstanceid
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
 - ISyncProviderRegistration::GetSyncProviderConfigUIFromInstanceId
 - syncregistration/ISyncProviderRegistration::GetSyncProviderConfigUIFromInstanceId
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
 - ISyncProviderRegistration.GetSyncProviderConfigUIFromInstanceId
---

# ISyncProviderRegistration::GetSyncProviderConfigUIFromInstanceId


## -description

Returns an initialized and instantiated  <a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderconfigui">ISyncProviderConfigUI</a> object for the given unique instance ID.

## -parameters

### -param pguidInstanceId [in]

The unique instance ID of the <b>ISyncProviderConfigUI</b> object.

### -param dwClsContext [in]

The context in which the code that manages the newly created object will run. The only context supported is <b>CLSCTX_INPROC_SERVER</b>.

### -param ppConfigUI [out]

The initialized and instantiated configuration UI object.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The instance ID is <b>GUID_NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough memory available to create the configuration UI.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
The synchronization provider’s CLSID is not registered with the requested context or the configuration UI has not had its DLL registered.

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

This method is used to obtain an <b>ISyncProviderConfigUIInfo</b> directly when the instance ID of the <b>ISyncProviderConfigUI</b> is known. The  <a href="/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderregistration-getsyncproviderconfiguiinfoforprovider">GetSyncProviderConfigUIInfoforProvider</a> method can be used to access an <b>ISyncProviderConfigUIInfo</b> object from the instance ID of a synchronization provider.

## -see-also

<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderconfigui">ISyncProviderConfigUI Interface</a>



<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderregistration">ISyncProviderRegistration Interface</a>