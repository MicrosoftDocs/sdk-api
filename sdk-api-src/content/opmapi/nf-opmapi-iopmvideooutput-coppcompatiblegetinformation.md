---
UID: NF:opmapi.IOPMVideoOutput.COPPCompatibleGetInformation
title: IOPMVideoOutput::COPPCompatibleGetInformation
author: windows-sdk-content
description: Sends an Output Protection Manager (OPM) status request to the display driver. Use this method when OPM is emulating Certified Output Protection Manager (COPP).
old-location: mf\iopmvideooutput_iopmvideooutput__coppcompatiblegetinformation.htm
tech.root: MedFound
ms.assetid: 46c0c426-9730-4a0e-ab95-03b240bd55f0
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: COPPCompatibleGetInformation, COPPCompatibleGetInformation method [Media Foundation], COPPCompatibleGetInformation method [Media Foundation],IOPMVideoOutput interface, IOPMVideoOutput interface [Media Foundation],COPPCompatibleGetInformation method, IOPMVideoOutput.COPPCompatibleGetInformation, IOPMVideoOutput::COPPCompatibleGetInformation, mf.iopmvideooutput_iopmvideooutput__coppcompatiblegetinformation, opmapi/IOPMVideoOutput::COPPCompatibleGetInformation
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
 - IOPMVideoOutput.COPPCompatibleGetInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOPMVideoOutput::COPPCompatibleGetInformation


## -description


Sends an Output Protection Manager (OPM) status request to the display driver. Use this method when OPM is emulating Certified Output Protection Manager (COPP).


## -parameters




### -param pParameters [in]

Pointer to an <a href="https://msdn.microsoft.com/60d13945-740f-46bd-9602-bacd0dac5e32">OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS</a> structure. Fill in this structure with data for the status request. For a list of status requests, see <a href="https://msdn.microsoft.com/428d08c6-e9f0-49fb-9ef9-d0f95416669d">OPM Status Requests</a>.


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

The <a href="https://msdn.microsoft.com/8bf43577-3535-4f62-ac81-bb7e3c329403">IOPMVideoOutput</a> interface supports both OPM semantics and COPP semantics. The <b>COPPCompatibleGetInformation</b> method applies only when COPP semantics are used. If the interface pointer was created with OPM semantics, <b>COPPCompatibleGetInformation</b> returns ERROR_GRAPHICS_OPM_VIDEO_OUTPUT_DOES_NOT_HAVE_COPP_SEMANTICS. In that case, call <a href="https://msdn.microsoft.com/47d724eb-07e9-4659-886a-4b492fbb2415">IOPMVideoOutput::GetInformation</a> instead.




## -see-also




<a href="https://msdn.microsoft.com/8bf43577-3535-4f62-ac81-bb7e3c329403">IOPMVideoOutput</a>



<a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>
 

 

