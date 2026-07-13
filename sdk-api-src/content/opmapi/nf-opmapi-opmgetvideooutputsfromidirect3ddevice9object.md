---
UID: NF:opmapi.OPMGetVideoOutputsFromIDirect3DDevice9Object
title: OPMGetVideoOutputsFromIDirect3DDevice9Object function (opmapi.h)
description: Creates an Output Protection Manager (OPM) object for each physical monitor that is associated with a particular Direct3D device.
helpviewer_keywords: ["OPMGetVideoOutputsFromIDirect3DDevice9Object","OPMGetVideoOutputsFromIDirect3DDevice9Object function [Media Foundation]","OPM_VOS_COPP_SEMANTICS","OPM_VOS_OPM_SEMANTICS","mf.opmgetvideooutputsfromidirect3ddevice9object","opmapi/OPMGetVideoOutputsFromIDirect3DDevice9Object"]
old-location: mf\opmgetvideooutputsfromidirect3ddevice9object.htm
tech.root: mf
ms.assetid: 9b287058-9e06-4c40-84f4-506aefce5b8a
ms.date: 12/05/2018
ms.keywords: OPMGetVideoOutputsFromIDirect3DDevice9Object, OPMGetVideoOutputsFromIDirect3DDevice9Object function [Media Foundation], OPM_VOS_COPP_SEMANTICS, OPM_VOS_OPM_SEMANTICS, mf.opmgetvideooutputsfromidirect3ddevice9object, opmapi/OPMGetVideoOutputsFromIDirect3DDevice9Object
req.header: opmapi.h
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
req.lib: Dxva2.lib
req.dll: Dxva2.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OPMGetVideoOutputsFromIDirect3DDevice9Object
 - opmapi/OPMGetVideoOutputsFromIDirect3DDevice9Object
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dxva2.dll
api_name:
 - OPMGetVideoOutputsFromIDirect3DDevice9Object
---

# OPMGetVideoOutputsFromIDirect3DDevice9Object function


## -description

Creates an Output Protection Manager (OPM) object for each physical monitor that is associated with a particular Direct3D device.

## -parameters

### -param pDirect3DDevice9 [in]

Pointer to the <b>IDirect3DDevice9</b> interface of a Direct3D device.

### -param vos [in]

A member of the <a href="/windows/desktop/api/opmapi/ne-opmapi-opm_video_output_semantics">OPM_VIDEO_OUTPUT_SEMANTICS</a> enumeration.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OPM_VOS_OPM_SEMANTICS"></a><a id="opm_vos_opm_semantics"></a><dl>
<dt><b>OPM_VOS_OPM_SEMANTICS</b></dt>
</dl>
</td>
<td width="60%">
The returned <a href="/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput">IOPMVideoOutput</a> pointers will use OPM semantics.

</td>
</tr>
<tr>
<td width="40%"><a id="OPM_VOS_COPP_SEMANTICS"></a><a id="opm_vos_copp_semantics"></a><dl>
<dt><b>OPM_VOS_COPP_SEMANTICS</b></dt>
</dl>
</td>
<td width="60%">
The returned <a href="/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput">IOPMVideoOutput</a> pointers will use Certified Output Protection Protocol (COPP) semantics.

</td>
</tr>
</table>

### -param pulNumVideoOutputs [out]

Receives the number of <a href="/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput">IOPMVideoOutput</a> pointers returned in the <i>pppOPMVideoOutputArray</i> parameter.

### -param pppOPMVideoOutputArray [out]

Receives a pointer to an array of <a href="/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput">IOPMVideoOutput</a> pointers. Each <b>IOPMVideoOutput</b> pointer is associated with a single physical monitor. The caller must release each pointer in the array, and call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to free the array.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A single Direct3D device can be associated with several physical monitors. Each physical monitor has its own connector. The application must set the protection mechanism individually for each physical monitor, by using the <a href="/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput">IOPMVideoOutput</a> pointers returned in <i>pppOPMVideoOutputArray</i>.

The <a href="/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput">IOPMVideoOutput</a> interface has two modes of behavior, depending on the value of the <i>vos</i> parameter. If <i>vos</i> is OPM_VOS_COPP_SEMANTICS, <b>IOPMVideoOutput</b> uses COPP semantics. This mode is intended for backward compatibility with COPP. If <i>vos</i> is OPM_VOS_OPM_SEMANTICS, <b>IOPMVideoOutput</b> uses the newer OPM semantics. Differences in behavior are noted on the reference page for each method. The mode does not change during the lifetime of the object.

## -see-also

<a href="/windows/desktop/medfound/opm-functions">OPM Functions</a>