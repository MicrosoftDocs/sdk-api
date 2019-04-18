---
UID: NF:syncregistration.ISyncProviderRegistration.EnumerateSyncProviderConfigUIs
title: ISyncProviderRegistration::EnumerateSyncProviderConfigUIs (syncregistration.h)
author: windows-sdk-content
description: Returns an IEnumSyncProviderConfigUIInfos enumeration interface that enumerates all registered ISyncProviderConfigUIInfo objects for the specified criteria.
old-location: winsync\isyncproviderregistration_enumeratesyncproviderconfiguis.htm
tech.root: winsync
ms.assetid: e3f87fc7-f123-454e-851c-92dbad605600
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumerateSyncProviderConfigUIs, EnumerateSyncProviderConfigUIs method [Windows Sync], EnumerateSyncProviderConfigUIs method [Windows Sync],ISyncProviderRegistration interface, ISyncProviderRegistration interface [Windows Sync],EnumerateSyncProviderConfigUIs method, ISyncProviderRegistration.EnumerateSyncProviderConfigUIs, ISyncProviderRegistration::EnumerateSyncProviderConfigUIs, syncregistration/ISyncProviderRegistration::EnumerateSyncProviderConfigUIs, winsync.isyncproviderregistration_enumeratesyncproviderconfiguis
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncregistration.h
api_name:
 - ISyncProviderRegistration.EnumerateSyncProviderConfigUIs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncProviderRegistration::EnumerateSyncProviderConfigUIs


## -description


Returns an <a href="https://msdn.microsoft.com/d8b4f4a4-b238-431f-a123-edebe07ea7b0">IEnumSyncProviderConfigUIInfos</a> enumeration interface that enumerates all registered <b>ISyncProviderConfigUIInfo</b> objects for the specified  criteria.


## -parameters




### -param pguidContentType [in]

The LPCGUID of the specified content type. If this parameter is <b>NULL</b>, all content types will be enumerated.


### -param dwSupportedArchitecture [in]

One, or a combination  of, the following flags that represent the architectures of the providers to be enumerated. If <b>SYNC_32_BIT_SUPPORTED</b> is specified, all providers that support 32 bits or 32 and 64 bits will be enumerated.  If <b>SYNC_32_BIT_SUPPORTED</b> | <b>SYNC_64_BIT_SUPPORTED</b> is specified, only those providers that support both 32 bits and 64 bits will be enumerated.

<ul>
<li><b>SYNC_32_BIT_SUPPORTED</b> ((DWORD)0x00000001)</li>
<li><b>SYNC_64_BIT_SUPPORTED</b>  ((DWORD)0x00000002)</li>
</ul>
If this parameter is set to zero, synchronization providers for all architectures will be enumerated.


### -param ppEnumSyncProviderConfigUIInfos

TBD




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
There was not enough memory available to register the provider.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/58b0dcc2-861a-4138-872a-cbbe2bb2cc4d">IEnumSyncProviderInfos Interface</a>



<a href="https://msdn.microsoft.com/e7cf0c05-9d07-4630-ae34-9a9dd81492b2">ISyncProviderRegistration Interface</a>
 

 

