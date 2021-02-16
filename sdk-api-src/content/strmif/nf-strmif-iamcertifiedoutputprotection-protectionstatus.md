---
UID: NF:strmif.IAMCertifiedOutputProtection.ProtectionStatus
title: IAMCertifiedOutputProtection::ProtectionStatus (strmif.h)
description: The ProtectionStatus method sends a COPP status request to the graphics driver.
helpviewer_keywords: ["IAMCertifiedOutputProtection interface [DirectShow]","ProtectionStatus method","IAMCertifiedOutputProtection.ProtectionStatus","IAMCertifiedOutputProtection::ProtectionStatus","IAMCertifiedOutputProtectionProtectionStatus","ProtectionStatus","ProtectionStatus method [DirectShow]","ProtectionStatus method [DirectShow]","IAMCertifiedOutputProtection interface","dshow.iamcertifiedoutputprotection_protectionstatus","strmif/IAMCertifiedOutputProtection::ProtectionStatus"]
old-location: dshow\iamcertifiedoutputprotection_protectionstatus.htm
tech.root: dshow
ms.assetid: c93ebbcc-ce44-4d77-b088-7112ddaf41b2
ms.date: 12/05/2018
ms.keywords: IAMCertifiedOutputProtection interface [DirectShow],ProtectionStatus method, IAMCertifiedOutputProtection.ProtectionStatus, IAMCertifiedOutputProtection::ProtectionStatus, IAMCertifiedOutputProtectionProtectionStatus, ProtectionStatus, ProtectionStatus method [DirectShow], ProtectionStatus method [DirectShow],IAMCertifiedOutputProtection interface, dshow.iamcertifiedoutputprotection_protectionstatus, strmif/IAMCertifiedOutputProtection::ProtectionStatus
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMCertifiedOutputProtection::ProtectionStatus
 - strmif/IAMCertifiedOutputProtection::ProtectionStatus
dev_langs:
 - c++
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
---

# IAMCertifiedOutputProtection::ProtectionStatus


## -description

The <code>ProtectionStatus</code> method sends a COPP status request to the graphics driver.

## -parameters

### -param pStatusInput [in]

Pointer to an [AMCOPPStatusInput](/windows/desktop/api/strmif/ns-strmif-amcoppstatusinput) structure that contains the status request.

### -param pStatusOutput [out]

Pointer to an [AMCOPPStatusOutput](/windows/desktop/api/strmif/ns-strmif-amcoppstatusoutput) structure. The method fills this structure with the driver's response.

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

<a href="/windows/desktop/api/strmif/nn-strmif-iamcertifiedoutputprotection">IAMCertifiedOutputProtection Interface</a>



<a href="/windows/desktop/DirectShow/using-certified-output-protection-protocol--copp">Using Certified Output Protection Protocol (COPP)</a>