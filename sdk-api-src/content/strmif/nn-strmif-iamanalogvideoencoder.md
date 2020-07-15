---
UID: NN:strmif.IAMAnalogVideoEncoder
title: IAMAnalogVideoEncoder (strmif.h)
description: Note  This interface has been deprecated. Note  Microsoft does not provide an implementation of this interface.
helpviewer_keywords: ["IAMAnalogVideoEncoder","IAMAnalogVideoEncoder interface [DirectShow]","IAMAnalogVideoEncoder interface [DirectShow]","described","IAMAnalogVideoEncoderInterface","dshow.iamanalogvideoencoder","strmif/IAMAnalogVideoEncoder"]
old-location: dshow\iamanalogvideoencoder.htm
tech.root: DirectShow
ms.assetid: fb2927cf-c979-411f-a896-d010b684acf2
ms.date: 12/05/2018
ms.keywords: IAMAnalogVideoEncoder, IAMAnalogVideoEncoder interface [DirectShow], IAMAnalogVideoEncoder interface [DirectShow],described, IAMAnalogVideoEncoderInterface, dshow.iamanalogvideoencoder, strmif/IAMAnalogVideoEncoder
f1_keywords:
- strmif/IAMAnalogVideoEncoder
dev_langs:
- c++
req.header: strmif.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- strmif.h
api_name:
- IAMAnalogVideoEncoder
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMAnalogVideoEncoder interface


## -description



<div class="alert"><b>Note</b>  This interface has been deprecated.</div>
<div> </div>
<div class="alert"><b>Note</b>  Microsoft does not provide an implementation of this interface. Third parties might implement it.</div>
<div> </div>
The <b>IAMAnalogVideoEncoder</b> interface might be implemented by a hardware video encoder in video capture operations when an application is streaming data to disk and sending it back out to videotape. 




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMAnalogVideoEncoder</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMAnalogVideoEncoder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMAnalogVideoEncoder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamanalogvideoencoder-get_availabletvformats">get_AvailableTVFormats</a>
</td>
<td align="left" width="63%">
Retrieves the analog video standards (NTSC/M, PAL/B, SECAM/K1, and so on) supported by the encoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamanalogvideoencoder-get_ccenable">get_CCEnable</a>
</td>
<td align="left" width="63%">
Determines whether closed captioning is currently enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamanalogvideoencoder-get_copyprotection">get_CopyProtection</a>
</td>
<td align="left" width="63%">
Determines whether copy protection is currently enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamanalogvideoencoder-get_tvformat">get_TVFormat</a>
</td>
<td align="left" width="63%">
Retrieves the analog video standard that the encoder is currently set to.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamanalogvideoencoder-put_ccenable">put_CCEnable</a>
</td>
<td align="left" width="63%">
Enables or disables closed captioning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamanalogvideoencoder-put_copyprotection">put_CopyProtection</a>
</td>
<td align="left" width="63%">
Sets the level of copy protection for the encoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamanalogvideoencoder-put_tvformat">put_TVFormat</a>
</td>
<td align="left" width="63%">
Sets the encoder to a particular analog video standard.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/deprecated-interfaces">Deprecated Interfaces</a>
 

 

