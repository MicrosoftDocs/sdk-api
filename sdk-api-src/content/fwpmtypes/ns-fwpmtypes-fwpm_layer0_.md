---
UID: NS:fwpmtypes.FWPM_LAYER0_
title: FWPM_LAYER0_
author: windows-driver-content
description: Schema information for a layer.
old-location: fwp\fwpm_layer0_struct.htm
old-project: FWP
ms.assetid: 77d567a7-9495-4f16-9b02-e44a1ef67022
ms.author: windowsdriverdev
ms.date: 4/12/2018
ms.keywords: FWPM_LAYER0, FWPM_LAYER0 structure [Filtering], FWPM_LAYER0_, FWPM_LAYER_FLAG_BUFFERED, FWPM_LAYER_FLAG_BUILTIN, FWPM_LAYER_FLAG_CLASSIFY_MOSTLY, FWPM_LAYER_FLAG_KERNEL, fwp.fwpm_layer0_struct, fwpmtypes/FWPM_LAYER0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FWPM_LAYER0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Fwpmtypes.h
api_name:
-	FWPM_LAYER0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FWPM_LAYER0_ structure


## -description



		The <b>FWPM_LAYER0</b> structure contains schema information for a layer.


## -struct-fields




### -field layerKey

Uniquely identifies the layer.


### -field displayData

Allows layers to be annotated in a human-readable form. The <b>name</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550081">FWPM_DISPLAY_DATA0</a> structure is not <b>NULL</b>.


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

See <a href="https://msdn.microsoft.com/30d68d48-156e-440b-8607-8b64cfa25049">FWPM_FIELD0</a> for more information.


### -field defaultSubLayerKey

Sublayer used when a filter is added with a null sublayer.


### -field layerId

LUID that identifies this layer.


## -remarks



<b>FWPM_LAYER0</b> is a specific implementation of FWPM_LAYER. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550081">FWPM_DISPLAY_DATA0</a>



<a href="https://msdn.microsoft.com/30d68d48-156e-440b-8607-8b64cfa25049">FWPM_FIELD0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

