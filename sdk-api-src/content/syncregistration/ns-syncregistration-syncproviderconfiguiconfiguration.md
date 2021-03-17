---
UID: NS:syncregistration._SyncProviderConfigUIConfiguration
title: SyncProviderConfigUIConfiguration (syncregistration.h)
description: Represents the information for a synchronization provider configuration UI.
helpviewer_keywords: ["SyncProviderConfigUI","SyncProviderConfigUI structure [Windows Sync]","SyncProviderConfigUIConfiguration","SyncProviderConfigUIConfiguration structure [Windows Sync]","syncregistration/SyncProviderConfigUI","winsync.syncproviderconfiguiconfiguration"]
old-location: winsync\syncproviderconfiguiconfiguration.htm
tech.root: winsync
ms.assetid: 4f07719b-c1e5-4985-a952-0ff07601bf1a
ms.date: 12/05/2018
ms.keywords: SyncProviderConfigUI, SyncProviderConfigUI structure [Windows Sync], SyncProviderConfigUIConfiguration, SyncProviderConfigUIConfiguration structure [Windows Sync], syncregistration/SyncProviderConfigUI, winsync.syncproviderconfiguiconfiguration
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
req.typenames: SyncProviderConfigUIConfiguration
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SyncProviderConfigUIConfiguration
 - syncregistration/_SyncProviderConfigUIConfiguration
 - SyncProviderConfigUIConfiguration
 - syncregistration/SyncProviderConfigUIConfiguration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Syncregistration.h
api_name:
 - SyncProviderConfigUI
---

# SyncProviderConfigUIConfiguration structure


## -description

Represents the information for a synchronization provider configuration UI.

## -struct-fields

### -field dwVersion

The version of the configuration UI.

### -field guidInstanceId

The unique instance ID of the configuration UI.

### -field clsidConfigUI

The COM CLSID of the configuration UI.

### -field guidContentType

The GUID that identifies the content type supported by the synchronization provider that is created by the configuration UI.

### -field dwCapabilities

One of the following constants that represent the capabilities of the synchronization provider configuration UI. These values are masks that can be combined.

<ul>
<li><b>SCC_DEFAULT</b> ((DWORD)0x00000000) The configuration UI supports the default capabilities of creating and modifying a synchronization provider with a UI displayed.

</li>
<li><b>SCC_CAN_CREATE_WITHOUT_UI</b>  ((DWORD)0x00000001) The configuration UI creates providers without displaying the UI.  This value is not compatible with <b>SCC_CREATE_NOT_SUPPORTED</b>.

</li>
<li><b>SCC_CAN_MODIFY_WITHOUT_UI</b>  ((DWORD)0x00000002) The configuration UI modifies providers without displaying the UI.  This value is not compatible with <b>SCC_MODIFY_NOT_SUPPORTED</b>.

</li>
<li><b>SCC_CREATE_NOT_SUPPORTED</b>  ((DWORD)0x00000004) The configuration UI cannot create new configured providers.  This value is not compatible with <b>SCC_CAN_CREATE_WITHOUT_UI</b>.

</li>
<li><b>SCC_MODIFY_NOT_SUPPORTED</b>  ((DWORD)0x00000008) The configuration UI cannot modify providers.  This value is not compatible with <b>SCC_CAN_MODIFY_WITHOUT_UI</b>.

</li>
</ul>

### -field dwSupportedArchitecture

One of the following constants that represent the architectures supported by the synchronization provider configuration UI. This value corresponds to the architectures that the synchronization provider configuration UI CLSID (<b>clsidConfigUI</b>) is registered for.   These values can be combined, and can be used as bitmasks.

<ul>
<li><b>SYNC_32_BIT_SUPPORTED</b> ((DWORD)0x00000001)</li>
<li><b>SYNC_64_BIT_SUPPORTED</b>  ((DWORD)0x00000002)</li>
</ul>

### -field fIsGlobal

Reserved for future use. At this time, the value should always be <b>FALSE</b>.

## -see-also

<a href="/previous-versions/windows/desktop/winsync/windows-sync-registration-structures">Windows Sync Registration Structures</a>