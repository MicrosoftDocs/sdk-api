---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

