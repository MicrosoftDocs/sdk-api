---
UID: NE:cfapi.CF_PLACEHOLDER_STATE
title: CF_PLACEHOLDER_STATE (cfapi.h)
description: The state of a placeholder file or folder.
helpviewer_keywords: ["CF_PLACEHOLDER_STATE","CF_PLACEHOLDER_STATE enumeration","CF_PLACEHOLDER_STATE_ESSENTIAL_PROP_PRESENT","CF_PLACEHOLDER_STATE_INVALID","CF_PLACEHOLDER_STATE_IN_SYNC","CF_PLACEHOLDER_STATE_NO_STATES","CF_PLACEHOLDER_STATE_PARTIAL","CF_PLACEHOLDER_STATE_PARTIALLY_ON_DISK","CF_PLACEHOLDER_STATE_PLACEHOLDER","CF_PLACEHOLDER_STATE_SYNC_ROOT","cfapi/CF_PLACEHOLDER_STATE","cfapi/CF_PLACEHOLDER_STATE_ESSENTIAL_PROP_PRESENT","cfapi/CF_PLACEHOLDER_STATE_INVALID","cfapi/CF_PLACEHOLDER_STATE_IN_SYNC","cfapi/CF_PLACEHOLDER_STATE_NO_STATES","cfapi/CF_PLACEHOLDER_STATE_PARTIAL","cfapi/CF_PLACEHOLDER_STATE_PARTIALLY_ON_DISK","cfapi/CF_PLACEHOLDER_STATE_PLACEHOLDER","cfapi/CF_PLACEHOLDER_STATE_SYNC_ROOT","cloudApi.cf_placeholder_state"]
old-location: cloudapi\cf_placeholder_state.htm
tech.root: cloudapi
ms.assetid: 5E814458-2045-4CFD-90AC-F1F53DEB4FD0
ms.date: 12/05/2018
ms.keywords: CF_PLACEHOLDER_STATE, CF_PLACEHOLDER_STATE enumeration, CF_PLACEHOLDER_STATE_ESSENTIAL_PROP_PRESENT, CF_PLACEHOLDER_STATE_INVALID, CF_PLACEHOLDER_STATE_IN_SYNC, CF_PLACEHOLDER_STATE_NO_STATES, CF_PLACEHOLDER_STATE_PARTIAL, CF_PLACEHOLDER_STATE_PARTIALLY_ON_DISK, CF_PLACEHOLDER_STATE_PLACEHOLDER, CF_PLACEHOLDER_STATE_SYNC_ROOT, cfapi/CF_PLACEHOLDER_STATE, cfapi/CF_PLACEHOLDER_STATE_ESSENTIAL_PROP_PRESENT, cfapi/CF_PLACEHOLDER_STATE_INVALID, cfapi/CF_PLACEHOLDER_STATE_IN_SYNC, cfapi/CF_PLACEHOLDER_STATE_NO_STATES, cfapi/CF_PLACEHOLDER_STATE_PARTIAL, cfapi/CF_PLACEHOLDER_STATE_PARTIALLY_ON_DISK, cfapi/CF_PLACEHOLDER_STATE_PLACEHOLDER, cfapi/CF_PLACEHOLDER_STATE_SYNC_ROOT, cloudApi.cf_placeholder_state
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CF_PLACEHOLDER_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_PLACEHOLDER_STATE
 - cfapi/CF_PLACEHOLDER_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CfApi.h
api_name:
 - CF_PLACEHOLDER_STATE
---

# CF_PLACEHOLDER_STATE enumeration


## -description

The state of a placeholder file or folder.

## -enum-fields

### -field CF_PLACEHOLDER_STATE_NO_STATES:0x00000000

When returned, the file or directory whose <i>FileAttributes</i> and <i>ReparseTag</i> examined by the API is not a placeholder.

### -field CF_PLACEHOLDER_STATE_PLACEHOLDER:0x00000001

The file or directory whose <i>FileAttributes</i> and <i>ReparseTag</i> examined by the API is a placeholder.

### -field CF_PLACEHOLDER_STATE_SYNC_ROOT:0x00000002

The directory is both a placeholder directory as well as the sync root.

### -field CF_PLACEHOLDER_STATE_ESSENTIAL_PROP_PRESENT:0x00000004

The file or directory must be a placeholder and there exists an essential property in the property store of the file or directory.

### -field CF_PLACEHOLDER_STATE_IN_SYNC:0x00000008

The file or directory must be a placeholder and its content in sync with the cloud.

### -field CF_PLACEHOLDER_STATE_PARTIAL:0x00000010

The file or directory must be a placeholder and its content is not ready to be consumed by the user application, though it may or may not be fully present locally. An example is a placeholder file whose content has been fully downloaded to the local disk, but is yet to be validated by a sync provider that has registered the sync root with the hydration modifier VERIFICATION_REQUIRED.

### -field CF_PLACEHOLDER_STATE_PARTIALLY_ON_DISK:0x00000020

The file or directory must be a placeholder and its content is not fully present locally. When this is set, <b>CF_PLACEHOLDER_STATE_PARTIAL</b> must also be set.

### -field CF_PLACEHOLDER_STATE_INVALID:0xffffffff

This is an invalid state when the API fails to parse the information of the file or directory.

## -remarks

Placeholder state information can be obtained by calling: <a href="/windows/desktop/api/cfapi/nf-cfapi-cfgetplaceholderstatefromattributetag">CfGetPlaceholderStateFromAttributeTag</a>, <a href="/windows/desktop/api/cfapi/nf-cfapi-cfgetplaceholderstatefromfileinfo">CfGetPlaceholderStateFromFileInfo</a>, or <a href="/windows/desktop/api/cfapi/nf-cfapi-cfgetplaceholderstatefromfinddata">CfGetPlaceholderStateFromFindData</a>.
