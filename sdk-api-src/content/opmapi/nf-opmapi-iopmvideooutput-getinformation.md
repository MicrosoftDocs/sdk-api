---
UID: NF:opmapi.IOPMVideoOutput.GetInformation
title: IOPMVideoOutput::GetInformation (opmapi.h)
description: Sends an Output Protection Manager (OPM) status request to the display driver.
helpviewer_keywords: ["GetInformation","GetInformation method [Media Foundation]","GetInformation method [Media Foundation]","IOPMVideoOutput interface","IOPMVideoOutput interface [Media Foundation]","GetInformation method","IOPMVideoOutput.GetInformation","IOPMVideoOutput::GetInformation","mf.iopmvideooutput_iopmvideooutput__getinformation","opmapi/IOPMVideoOutput::GetInformation"]
old-location: mf\iopmvideooutput_iopmvideooutput__getinformation.htm
tech.root: mf
ms.assetid: 47d724eb-07e9-4659-886a-4b492fbb2415
ms.date: 12/05/2018
ms.keywords: GetInformation, GetInformation method [Media Foundation], GetInformation method [Media Foundation],IOPMVideoOutput interface, IOPMVideoOutput interface [Media Foundation],GetInformation method, IOPMVideoOutput.GetInformation, IOPMVideoOutput::GetInformation, mf.iopmvideooutput_iopmvideooutput__getinformation, opmapi/IOPMVideoOutput::GetInformation
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
 - IOPMVideoOutput::GetInformation
 - opmapi/IOPMVideoOutput::GetInformation
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
 - IOPMVideoOutput.GetInformation
---

# IOPMVideoOutput::GetInformation


## -description

Sends an Output Protection Manager (OPM) status request to the display driver.

## -parameters

### -param pParameters [in]

Pointer to an <a href="/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters">OPM_GET_INFO_PARAMETERS</a> structure. Fill in this structure with data for the status request. For a list of status requests, see <a href="/windows/desktop/medfound/opm-status-requests">OPM Status Requests</a>.

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
<dt><b>ERROR_GRAPHICS_OPM_VIDEO_OUTPUT_DOES_NOT_HAVE_OPM_SEMANTICS</b></dt>
</dl>
</td>
<td width="60%">
The OPM object was created with Certified Output Protection Protocol (COPP) semantics.

</td>
</tr>
</table>

## -remarks

This method is equivalent to the <b>IAMCertifiedOutputProtection::ProtectionStatus</b> method in COPP.

The <a href="/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput">IOPMVideoOutput</a> interface supports both OPM semantics and COPP semantics. The <b>GetInformation</b> method applies only when OPM semantics are used. If the interface pointer was created with COPP semantics, <b>GetInformation</b> returns ERROR_GRAPHICS_OPM_VIDEO_OUTPUT_DOES_NOT_HAVE_OPM_SEMANTICS. In that case, call <a href="/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation">IOPMVideoOutput::COPPCompatibleGetInformation</a> instead.

## -see-also

<a href="/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput">IOPMVideoOutput</a>



<a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>