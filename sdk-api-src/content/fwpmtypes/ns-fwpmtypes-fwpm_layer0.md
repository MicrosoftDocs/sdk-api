---
UID: NS:fwpmtypes.FWPM_LAYER0_
title: FWPM_LAYER0 (fwpmtypes.h)
description: Schema information for a layer.
helpviewer_keywords: ["FWPM_LAYER0","FWPM_LAYER0 structure [Filtering]","FWPM_LAYER_FLAG_BUFFERED","FWPM_LAYER_FLAG_BUILTIN","FWPM_LAYER_FLAG_CLASSIFY_MOSTLY","FWPM_LAYER_FLAG_KERNEL","fwp.fwpm_layer0_struct","fwpmtypes/FWPM_LAYER0"]
old-location: fwp\fwpm_layer0_struct.htm
tech.root: fwp
ms.assetid: 77d567a7-9495-4f16-9b02-e44a1ef67022
ms.date: 12/05/2018
ms.keywords: FWPM_LAYER0, FWPM_LAYER0 structure [Filtering], FWPM_LAYER_FLAG_BUFFERED, FWPM_LAYER_FLAG_BUILTIN, FWPM_LAYER_FLAG_CLASSIFY_MOSTLY, FWPM_LAYER_FLAG_KERNEL, fwp.fwpm_layer0_struct, fwpmtypes/FWPM_LAYER0
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: FWPM_LAYER0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_LAYER0_
 - fwpmtypes/FWPM_LAYER0_
 - FWPM_LAYER0
 - fwpmtypes/FWPM_LAYER0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_LAYER0
---

# FWPM_LAYER0 structure


## -description

The <b>FWPM_LAYER0</b> structure contains schema information for a layer.

## -struct-fields

### -field layerKey

Uniquely identifies the layer.

### -field displayData

Allows layers to be annotated in a human-readable form. The [FWPM_DISPLAY_DATA0](/windows/desktop/api/fwptypes/ns-fwptypes-fwpm_display_data0) structure is not <b>NULL</b>.

### -field flags

Possible values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FWPM_LAYER_FLAG_KERNEL"></a><a id="fwpm_layer_flag_kernel"></a><dl>
<dt><b>FWPM_LAYER_FLAG_KERNEL</b></dt>
</dl>
</td>
<td width="60%">
Layer classified in kernel-mode.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_LAYER_FLAG_BUILTIN"></a><a id="fwpm_layer_flag_builtin"></a><dl>
<dt><b>FWPM_LAYER_FLAG_BUILTIN</b></dt>
</dl>
</td>
<td width="60%">
Layer built-in. Cannot be deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_LAYER_FLAG_CLASSIFY_MOSTLY"></a><a id="fwpm_layer_flag_classify_mostly"></a><dl>
<dt><b>FWPM_LAYER_FLAG_CLASSIFY_MOSTLY</b></dt>
</dl>
</td>
<td width="60%">
Layer optimized for classification rather than enumeration.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_LAYER_FLAG_BUFFERED"></a><a id="fwpm_layer_flag_buffered"></a><dl>
<dt><b>FWPM_LAYER_FLAG_BUFFERED</b></dt>
</dl>
</td>
<td width="60%">
Layer is buffered.

</td>
</tr>
</table>

### -field numFields

Number of fields in the layer.

### -field field

Schema information for the layer's fields.

See [FWPM_FIELD0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_field0) for more information.

### -field defaultSubLayerKey

Sublayer used when a filter is added with a null sublayer.

### -field layerId

LUID that identifies this layer.

## -remarks

<b>FWPM_LAYER0</b> is a specific implementation of FWPM_LAYER. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_DISPLAY_DATA0](/windows/desktop/api/fwptypes/ns-fwptypes-fwpm_display_data0)



[FWPM_FIELD0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_field0)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>