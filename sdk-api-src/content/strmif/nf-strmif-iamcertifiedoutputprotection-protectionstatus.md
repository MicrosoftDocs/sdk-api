---
UID: NF:strmif.IAMCertifiedOutputProtection.ProtectionStatus
title: IAMCertifiedOutputProtection::ProtectionStatus
author: windows-sdk-content
description: The ProtectionStatus method sends a COPP status request to the graphics driver.
old-location: dshow\iamcertifiedoutputprotection_protectionstatus.htm
old-project: DirectShow
ms.assetid: c93ebbcc-ce44-4d77-b088-7112ddaf41b2
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IAMCertifiedOutputProtection interface [DirectShow],ProtectionStatus method, IAMCertifiedOutputProtection.ProtectionStatus, IAMCertifiedOutputProtection::ProtectionStatus, IAMCertifiedOutputProtectionProtectionStatus, ProtectionStatus, ProtectionStatus method [DirectShow], ProtectionStatus method [DirectShow],IAMCertifiedOutputProtection interface, dshow.iamcertifiedoutputprotection_protectionstatus, strmif/IAMCertifiedOutputProtection::ProtectionStatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMCertifiedOutputProtection.ProtectionStatus
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMCertifiedOutputProtection::ProtectionStatus


## -description


The <code>ProtectionStatus</code> method sends a COPP status request to the graphics driver.


## -parameters




### -param pStatusInput [in]

Pointer to an <a href="https://msdn.microsoft.com/988e6d54-f241-4cfc-8793-fc42de92ac52">AMCOPPStatusInput</a> structure that contains the status request.


### -param pStatusOutput [out]

Pointer to an <a href="https://msdn.microsoft.com/136ce182-24c3-489d-a9c2-0121593e4b1e">AMCOPPStatusOutput</a> structure. The method fills this structure with the driver's response.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Invalid state. Possibly the application passed unexpected data, or called <b>IAMCertifiedOutputProtection</b> methods in the wrong order.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NO_COPP_HW</b></dt>
</dl>
</td>
<td width="60%">
The display device does not support COPP; or the VMR has not connected to a display device yet.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e5da271d-9528-4bcb-8b76-56fbec2e5855">IAMCertifiedOutputProtection Interface</a>



<a href="https://msdn.microsoft.com/23eebe93-416b-48c8-a05f-019e38b9a660">Using Certified Output Protection Protocol (COPP)</a>
 

 

