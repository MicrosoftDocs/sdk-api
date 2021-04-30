---
UID: NF:strmif.IAMCertifiedOutputProtection.ProtectionCommand
title: IAMCertifiedOutputProtection::ProtectionCommand (strmif.h)
description: The ProtectionCommand method sends a COPP command to the graphics driver.
helpviewer_keywords: ["IAMCertifiedOutputProtection interface [DirectShow]","ProtectionCommand method","IAMCertifiedOutputProtection.ProtectionCommand","IAMCertifiedOutputProtection::ProtectionCommand","IAMCertifiedOutputProtectionProtectionCommand","ProtectionCommand","ProtectionCommand method [DirectShow]","ProtectionCommand method [DirectShow]","IAMCertifiedOutputProtection interface","dshow.iamcertifiedoutputprotection_protectioncommand","strmif/IAMCertifiedOutputProtection::ProtectionCommand"]
old-location: dshow\iamcertifiedoutputprotection_protectioncommand.htm
tech.root: dshow
ms.assetid: facf13b2-6650-4e81-97ba-eadacc514ef0
ms.date: 12/05/2018
ms.keywords: IAMCertifiedOutputProtection interface [DirectShow],ProtectionCommand method, IAMCertifiedOutputProtection.ProtectionCommand, IAMCertifiedOutputProtection::ProtectionCommand, IAMCertifiedOutputProtectionProtectionCommand, ProtectionCommand, ProtectionCommand method [DirectShow], ProtectionCommand method [DirectShow],IAMCertifiedOutputProtection interface, dshow.iamcertifiedoutputprotection_protectioncommand, strmif/IAMCertifiedOutputProtection::ProtectionCommand
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
 - IAMCertifiedOutputProtection::ProtectionCommand
 - strmif/IAMCertifiedOutputProtection::ProtectionCommand
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
 - IAMCertifiedOutputProtection.ProtectionCommand
---

# IAMCertifiedOutputProtection::ProtectionCommand


## -description

The <code>ProtectionCommand</code> method sends a COPP command to the graphics driver.

## -parameters

### -param cmd [in]

Pointer to an [AMCOPPCommand](/windows/desktop/api/strmif/ns-strmif-amcoppcommand) structure that contains the command.

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