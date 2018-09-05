---
UID: NF:syncregistration.ISyncProviderConfigUIInfo.GetSyncProviderConfigUI
title: ISyncProviderConfigUIInfo::GetSyncProviderConfigUI
author: windows-sdk-content
description: Creates an instance of a synchronization provider configuration UI.
old-location: winsync\isyncproviderconfiguiinfo_getsyncproviderconfigui.htm
old-project: winsync
ms.assetid: eb9a2f2f-4c9f-405c-90f6-b251ab1a652d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetSyncProviderConfigUI, GetSyncProviderConfigUI method [Windows Sync], GetSyncProviderConfigUI method [Windows Sync],ISyncProviderConfigUIInfo interface, ISyncProviderConfigUIInfo interface [Windows Sync],GetSyncProviderConfigUI method, ISyncProviderConfigUIInfo.GetSyncProviderConfigUI, ISyncProviderConfigUIInfo::GetSyncProviderConfigUI, syncregistration/ISyncProviderConfigUIInfo::GetSyncProviderConfigUI, winsync.isyncproviderconfiguiinfo_getsyncproviderconfigui
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: syncregistration.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SYNC_REGISTRATION_EVENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncregistration.h
api_name:
 - ISyncProviderConfigUIInfo.GetSyncProviderConfigUI
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncProviderConfigUIInfo::GetSyncProviderConfigUI


## -description


Creates an instance of a synchronization provider configuration UI.


## -parameters




### -param dwClsContext [in]

The context in which the code that manages the newly created object will run. The only context supported is <b>CLSCTX_INPROC_SERVER</b>.


### -param ppSyncProviderConfigUI [out]

The instance of the synchronization provider configuration UI.


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
There was not enough memory available to create the configuration UI.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_DATA)</b></dt>
</dl>
</td>
<td width="60%">
Information stored in the registration store is an unexpected size.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b7c49533-d289-44b0-9a9e-cfa47af3a087">ISyncProviderConfigUIInfo Interface</a>
 

 

