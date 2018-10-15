---
UID: NF:opmapi.IOPMVideoOutput.GetInformation
title: IOPMVideoOutput::GetInformation
author: windows-sdk-content
description: Sends an Output Protection Manager (OPM) status request to the display driver.
old-location: mf\iopmvideooutput_iopmvideooutput__getinformation.htm
tech.root: medfound
ms.assetid: 47d724eb-07e9-4659-886a-4b492fbb2415
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetInformation, GetInformation method [Media Foundation], GetInformation method [Media Foundation],IOPMVideoOutput interface, IOPMVideoOutput interface [Media Foundation],GetInformation method, IOPMVideoOutput.GetInformation, IOPMVideoOutput::GetInformation, mf.iopmvideooutput_iopmvideooutput__getinformation, opmapi/IOPMVideoOutput::GetInformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - opmapi.h
api_name:
 - IOPMVideoOutput.GetInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOPMVideoOutput::GetInformation


## -description


Sends an Output Protection Manager (OPM) status request to the display driver.


## -parameters




### -param pParameters [in]

Pointer to an <a href="https://msdn.microsoft.com/8959c7d1-9a78-497f-8841-d3e61e9db6a3">OPM_GET_INFO_PARAMETERS</a> structure. Fill in this structure with data for the status request. For a list of status requests, see <a href="https://msdn.microsoft.com/428d08c6-e9f0-49fb-9ef9-d0f95416669d">OPM Status Requests</a>.


### -param pRequestedInformation [out]

Pointer to an <a href="https://msdn.microsoft.com/84ffa808-1bdb-47c8-a18c-6dfa6fcf90de">OPM_REQUESTED_INFORMATION</a> structure. On return, the method fills in this structure with the results of the status request.


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

The <a href="https://msdn.microsoft.com/8bf43577-3535-4f62-ac81-bb7e3c329403">IOPMVideoOutput</a> interface supports both OPM semantics and COPP semantics. The <b>GetInformation</b> method applies only when OPM semantics are used. If the interface pointer was created with COPP semantics, <b>GetInformation</b> returns ERROR_GRAPHICS_OPM_VIDEO_OUTPUT_DOES_NOT_HAVE_OPM_SEMANTICS. In that case, call <a href="https://msdn.microsoft.com/46c0c426-9730-4a0e-ab95-03b240bd55f0">IOPMVideoOutput::COPPCompatibleGetInformation</a> instead.




## -see-also




<a href="https://msdn.microsoft.com/8bf43577-3535-4f62-ac81-bb7e3c329403">IOPMVideoOutput</a>



<a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>
 

 

