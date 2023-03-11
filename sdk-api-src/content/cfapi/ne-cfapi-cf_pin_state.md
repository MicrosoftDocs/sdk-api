---
UID: NE:cfapi.CF_PIN_STATE
title: CF_PIN_STATE (cfapi.h)
description: Pin states of a placeholder file or directory.
helpviewer_keywords: ["CF_PIN_STATE","CF_PIN_STATE enumeration","CF_PIN_STATE_EXCLUDED","CF_PIN_STATE_INHERIT","CF_PIN_STATE_PINNED","CF_PIN_STATE_UNPINNED","CF_PIN_STATE_UNSPECIFIED","cfapi/CF_PIN_STATE","cfapi/CF_PIN_STATE_EXCLUDED","cfapi/CF_PIN_STATE_INHERIT","cfapi/CF_PIN_STATE_PINNED","cfapi/CF_PIN_STATE_UNPINNED","cfapi/CF_PIN_STATE_UNSPECIFIED","cloudApi.cf_pin_state"]
old-location: cloudapi\cf_pin_state.htm
tech.root: cloudapi
ms.assetid: F3074C9A-2805-47DE-9BA0-D7E02C4FF030
ms.date: 12/05/2018
ms.keywords: CF_PIN_STATE, CF_PIN_STATE enumeration, CF_PIN_STATE_EXCLUDED, CF_PIN_STATE_INHERIT, CF_PIN_STATE_PINNED, CF_PIN_STATE_UNPINNED, CF_PIN_STATE_UNSPECIFIED, cfapi/CF_PIN_STATE, cfapi/CF_PIN_STATE_EXCLUDED, cfapi/CF_PIN_STATE_INHERIT, cfapi/CF_PIN_STATE_PINNED, cfapi/CF_PIN_STATE_UNPINNED, cfapi/CF_PIN_STATE_UNSPECIFIED, cloudApi.cf_pin_state
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
req.typenames: CF_PIN_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_PIN_STATE
 - cfapi/CF_PIN_STATE
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
 - CF_PIN_STATE
---

# CF_PIN_STATE enumeration


## -description

Pin states of a placeholder file or directory.

## -enum-fields

### -field CF_PIN_STATE_UNSPECIFIED:0

The platform can decide freely when the placeholder’s content needs to present or absent locally on the disk.

### -field CF_PIN_STATE_PINNED:1

The sync provider will be notified to fetch the placeholder’s content asynchronously after the pin request is received by the platform. There is no guarantee that the placeholders to be pinned will be fully available locally after a <a href="/windows/desktop/api/cfapi/nf-cfapi-cfsetpinstate">CfSetPinState</a> call completes successfully. However, the platform will fail any dehydration request on pinned placeholders.

### -field CF_PIN_STATE_UNPINNED:2

The sync provider will be notified to dehydrate/invalidate the placeholder’s content on-disk asynchronously after the unpin request is received by the platform. There is no guarantee that the placeholders to be unpinned will be fully dehydrated after the API call completes successfully.

### -field CF_PIN_STATE_EXCLUDED:3

the placeholder will never be synced to the cloud by the sync provider. This state can only be set by the sync provider.

### -field CF_PIN_STATE_INHERIT:4  

The platform treats it as if the caller performs a move operation on the placeholder and hence re-evaluates the placeholder’s pin state based on its parent’s pin state. See the Remarks section for an inheritance table.

## -remarks

<table>
<tr>
<th></th>
<th>Parent</th>
<th>Unspecified</th>
<th>Pinned</th>
<th>Unpinned</th>
<th>Excluded</th>
</tr>
<tr>
<th>File</th>
<td>Unspecified</td>
<td>Unspecified</td>
<td>Pinned</td>
<td>Unspecified</td>
<td>Excluded</td>
</tr>
<tr>
<th></th>
<td>Pinned</td>
<td>Pinned</td>
<td>Pinned</td>
<td>Pinned</td>
<td>Excluded</td>
</tr>
<tr>
<th></th>
<td>Unpinned</td>
<td>Unpinned</td>
<td>Unpinned</td>
<td>Unpinned</td>
<td>Excluded</td>
</tr>
<tr>
<th></th>
<td>Excluded</td>
<td>Unspecified</td>
<td>Pinned</td>
<td>Unspecified</td>
<td>Excluded</td>
</tr>
<tr>
<th>Directory</th>
<td>Unspecified</td>
<td>Unspecified</td>
<td>Pinned</td>
<td>Unpinned</td>
<td>Excluded</td>
</tr>
<tr>
<th></th>
<td>Pinned</td>
<td>Pinned</td>
<td>Pinned</td>
<td>Pinned</td>
<td>Excluded</td>
</tr>
<tr>
<th></th>
<td>Unpinned</td>
<td>Unpinned</td>
<td>Unpinned</td>
<td>Unpinned</td>
<td>Excluded</td>
</tr>
<tr>
<th></th>
<td>Excluded</td>
<td>Unspecified</td>
<td>Pinned</td>
<td>Unpinned</td>
<td>Excluded</td>
</tr>
</table>
