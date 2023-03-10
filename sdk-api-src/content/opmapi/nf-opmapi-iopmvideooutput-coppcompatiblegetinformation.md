---
UID: NF:opmapi.IOPMVideoOutput.COPPCompatibleGetInformation
title: IOPMVideoOutput::COPPCompatibleGetInformation (opmapi.h)
description: Sends an Output Protection Manager (OPM) status request to the display driver. Use this method when OPM is emulating Certified Output Protection Manager (COPP).
helpviewer_keywords: ["COPPCompatibleGetInformation","COPPCompatibleGetInformation method [Media Foundation]","COPPCompatibleGetInformation method [Media Foundation]","IOPMVideoOutput interface","IOPMVideoOutput interface [Media Foundation]","COPPCompatibleGetInformation method","IOPMVideoOutput.COPPCompatibleGetInformation","IOPMVideoOutput::COPPCompatibleGetInformation","mf.iopmvideooutput_iopmvideooutput__coppcompatiblegetinformation","opmapi/IOPMVideoOutput::COPPCompatibleGetInformation"]
old-location: mf\iopmvideooutput_iopmvideooutput__coppcompatiblegetinformation.htm
tech.root: mf
ms.assetid: 46c0c426-9730-4a0e-ab95-03b240bd55f0
ms.date: 12/05/2018
ms.keywords: COPPCompatibleGetInformation, COPPCompatibleGetInformation method [Media Foundation], COPPCompatibleGetInformation method [Media Foundation],IOPMVideoOutput interface, IOPMVideoOutput interface [Media Foundation],COPPCompatibleGetInformation method, IOPMVideoOutput.COPPCompatibleGetInformation, IOPMVideoOutput::COPPCompatibleGetInformation, mf.iopmvideooutput_iopmvideooutput__coppcompatiblegetinformation, opmapi/IOPMVideoOutput::COPPCompatibleGetInformation
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOPMVideoOutput::COPPCompatibleGetInformation
 - opmapi/IOPMVideoOutput::COPPCompatibleGetInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - opmapi.h
api_name:
 - IOPMVideoOutput.COPPCompatibleGetInformation
---

# IOPMVideoOutput::COPPCompatibleGetInformation


## -description

Sends an Output Protection Manager (OPM) status request to the display driver. Use this method when OPM is emulating Certified Output Protection Manager (COPP).

## -parameters

### -param pParameters [in]

Pointer to an <a href="/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters">OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS</a> structure. Fill in this structure with data for the status request. For a list of status requests, see <a href="/windows/desktop/medfound/opm-status-requests">OPM Status Requests</a>.

### -param pRequestedInformation [out]

Pointer to an <a href="/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information">OPM_REQUESTED_INFORMATION</a> structure. On return, the method fills in this structure with the results of the status request.

## -returns

Returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<dt><b>ERROR_GRAPHICS_OPM_VIDEO_OUTPUT_DOES_NOT_HAVE_COPP_SEMANTICS</b></dt>
</dl>
</td>
<td width="60%">
The OPM object was created with OPM semantics, not COPP semantics.

</td>
</tr>
</table>

## -remarks

This method is equivalent to the <b>IAMCertifiedOutputProtection::ProtectionStatus</b> method in COPP.

The <a href="/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput">IOPMVideoOutput</a> interface supports both OPM semantics and COPP semantics. The <b>COPPCompatibleGetInformation</b> method applies only when COPP semantics are used. If the interface pointer was created with OPM semantics, <b>COPPCompatibleGetInformation</b> returns ERROR_GRAPHICS_OPM_VIDEO_OUTPUT_DOES_NOT_HAVE_COPP_SEMANTICS. In that case, call <a href="/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation">IOPMVideoOutput::GetInformation</a> instead.

## -see-also

<a href="/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput">IOPMVideoOutput</a>



<a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>