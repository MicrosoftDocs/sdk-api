---
UID: NE:cfapi.CF_PLACEHOLDER_STATE
title: CF_PLACEHOLDER_STATE
author: windows-sdk-content
description: The state of a placeholder file or folder.
old-location: cloudapi\cf_placeholder_state.htm
old-project: cfApi
ms.assetid: 5E814458-2045-4CFD-90AC-F1F53DEB4FD0
ms.author: windowssdkdev
ms.date: 02/26/2018
ms.keywords: CF_PLACEHOLDER_STATE, CF_PLACEHOLDER_STATE enumeration, CF_PLACEHOLDER_STATE_ESSENTIAL_PROP_PRESENT, CF_PLACEHOLDER_STATE_INVALID, CF_PLACEHOLDER_STATE_IN_SYNC, CF_PLACEHOLDER_STATE_NO_STATES, CF_PLACEHOLDER_STATE_PARTIAL, CF_PLACEHOLDER_STATE_PARTIALLY_ON_DISK, CF_PLACEHOLDER_STATE_PLACEHOLDER, CF_PLACEHOLDER_STATE_SYNC_ROOT, cfapi/CF_PLACEHOLDER_STATE, cfapi/CF_PLACEHOLDER_STATE_ESSENTIAL_PROP_PRESENT, cfapi/CF_PLACEHOLDER_STATE_INVALID, cfapi/CF_PLACEHOLDER_STATE_IN_SYNC, cfapi/CF_PLACEHOLDER_STATE_NO_STATES, cfapi/CF_PLACEHOLDER_STATE_PARTIAL, cfapi/CF_PLACEHOLDER_STATE_PARTIALLY_ON_DISK, cfapi/CF_PLACEHOLDER_STATE_PLACEHOLDER, cfapi/CF_PLACEHOLDER_STATE_SYNC_ROOT, cloudApi.cf_placeholder_state
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: CF_PLACEHOLDER_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CfApi.h
api_name:
 - CF_PLACEHOLDER_STATE
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
---

# CF_PLACEHOLDER_STATE enumeration


## -description


The state of a placeholder file or folder.


## -enum-fields




### -field CF_PLACEHOLDER_STATE_NO_STATES

When returned, the file or directory whose <i>FileAttributes</i> and <i>ReparseTag</i> examined by the API is not a placeholder.


### -field CF_PLACEHOLDER_STATE_PLACEHOLDER

The file or directory whose <i>FileAttributes</i> and <i>ReparseTag</i> examined by the API is a placeholder.


### -field CF_PLACEHOLDER_STATE_SYNC_ROOT

The directory is both a placeholder directory as well as the sync root.


### -field CF_PLACEHOLDER_STATE_ESSENTIAL_PROP_PRESENT

The file or directory must be a placeholder and there exists an essential property in the property store of the file or directory.


### -field CF_PLACEHOLDER_STATE_IN_SYNC

The file or directory must be a placeholder and its content in sync with the cloud.


### -field CF_PLACEHOLDER_STATE_PARTIAL

The file or directory must be a placeholder and its content is not ready to be consumed by the user application, though it may or may not be fully present locally. An example is a placeholder file whose content has been fully downloaded to the local disk, but is yet to be validated by a sync provider that has registered the sync root with the hydration modifier VERIFICATION_REQUIRED.


### -field CF_PLACEHOLDER_STATE_PARTIALLY_ON_DISK

The file or directory must be a placeholder and its content is not fully present locally. When this is set, <b>CF_PLACEHOLDER_STATE_PARTIAL</b> must also be set.


### -field CF_PLACEHOLDER_STATE_INVALID

This is an invalid state when the API fails to parse the information of the file or directory.


## -remarks



Placeholder state information can be obtained by calling: <a href="https://msdn.microsoft.com/D7B4FB60-3388-489F-9F55-153B53BBDA9F">CfGetPlaceholderStateFromAttributeTag</a>, <a href="https://msdn.microsoft.com/33DB8FAC-D2C9-4BBB-8505-1D9A680EA2BF">CfGetPlaceholderStateFromFileInfo</a>, or <a href="https://msdn.microsoft.com/1A8104BC-E9D1-4846-B91F-4CBEDB1FC542">CfGetPlaceholderStateFromFindData</a>.



