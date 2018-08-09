---
UID: NN:strmif.IAMAnalogVideoEncoder
title: IAMAnalogVideoEncoder
author: windows-sdk-content
description: Note  This interface has been deprecated. Note  Microsoft does not provide an implementation of this interface.
old-location: dshow\iamanalogvideoencoder.htm
old-project: DirectShow
ms.assetid: fb2927cf-c979-411f-a896-d010b684acf2
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IAMAnalogVideoEncoder, IAMAnalogVideoEncoder interface [DirectShow], IAMAnalogVideoEncoder interface [DirectShow],described, IAMAnalogVideoEncoderInterface, dshow.iamanalogvideoencoder, strmif/IAMAnalogVideoEncoder
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmif.h
api_name:
 - IAMAnalogVideoEncoder
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMAnalogVideoEncoder interface


## -description



<div class="alert"><b>Note</b>  This interface has been deprecated.</div>
<div> </div>
<div class="alert"><b>Note</b>  Microsoft does not provide an implementation of this interface. Third parties might implement it.</div>
<div> </div>
The <b>IAMAnalogVideoEncoder</b> interface might be implemented by a hardware video encoder in video capture operations when an application is streaming data to disk and sending it back out to videotape. 




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMAnalogVideoEncoder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMAnalogVideoEncoder</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/739a5f6f-2498-49f4-9c9d-008bd71d4855">get_AvailableTVFormats</a>
</td>
<td align="left" width="63%">
Retrieves the analog video standards (NTSC/M, PAL/B, SECAM/K1, and so on) supported by the encoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0dab4b3a-f139-4ac5-ab30-f223e9120c44">get_CCEnable</a>
</td>
<td align="left" width="63%">
Determines whether closed captioning is currently enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3eedb123-c70e-4a9a-98a9-abf7ccad32dc">get_CopyProtection</a>
</td>
<td align="left" width="63%">
Determines whether copy protection is currently enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a88e2e7-508b-448b-ac1d-50a50b4bb79a">get_TVFormat</a>
</td>
<td align="left" width="63%">
Retrieves the analog video standard that the encoder is currently set to.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6513cde7-2765-4225-814b-a619d6a6ab15">put_CCEnable</a>
</td>
<td align="left" width="63%">
Enables or disables closed captioning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2a762f3-8b11-4334-979d-206234d6cf09">put_CopyProtection</a>
</td>
<td align="left" width="63%">
Sets the level of copy protection for the encoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76109fa1-2f7a-4538-9755-6e2de5852d4b">put_TVFormat</a>
</td>
<td align="left" width="63%">
Sets the encoder to a particular analog video standard.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5b798477-9b36-4f59-b9cc-2938b5e4009f">Deprecated Interfaces</a>
 

 

