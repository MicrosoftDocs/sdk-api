---
UID: NF:strmif.IDvdControl2.SelectKaraokeAudioPresentationMode
title: IDvdControl2::SelectKaraokeAudioPresentationMode
author: windows-driver-content
description: The SelectKaraokeAudioPresentationMode method sends karaoke auxiliary channels to the left or right speakers.
old-location: dshow\idvdcontrol2_selectkaraokeaudiopresentationmode.htm
old-project: DirectShow
ms.assetid: 9101fd83-1349-4cdd-b5e9-6daeb7d1e3d8
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IDvdControl2 interface [DirectShow],SelectKaraokeAudioPresentationMode method, IDvdControl2.SelectKaraokeAudioPresentationMode, IDvdControl2::SelectKaraokeAudioPresentationMode, IDvdControl2SelectKaraokeAudioPresentationMode, SelectKaraokeAudioPresentationMode, SelectKaraokeAudioPresentationMode method [DirectShow], SelectKaraokeAudioPresentationMode method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_selectkaraokeaudiopresentationmode, strmif/IDvdControl2::SelectKaraokeAudioPresentationMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IDvdControl2.SelectKaraokeAudioPresentationMode
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdControl2::SelectKaraokeAudioPresentationMode


## -description



The <code>SelectKaraokeAudioPresentationMode</code> method sends karaoke auxiliary channels to the left or right speakers.




## -parameters




### -param ulMode [in]

Bitwise OR of <a href="https://msdn.microsoft.com/7f0132ae-6a46-4b81-9c5b-a0399a429b1a">DVD_KARAOKE_DOWNMIX</a> enumeration indicating how to downmix the five karaoke channels to channels 0 and 1, which are usually output to the left and right speakers.


## -returns



Returns one of the following values.

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
<dt><b>E_PROP_SET_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The audio decoder does not support downmixing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> filter is in an invalid domain.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
UOP control prohibits the current operation.

</td>
</tr>
</table>
 




## -remarks



When the DVD Navigator enters karaoke mode, it queries the audio decoder to discover whether it supports karaoke downmixing. If the decoder supports it, then channels 2 through 4 (the karaoke auxiliary channels with the guide vocals, guide melodies, and sound effects) are muted. Use this method to turn individual channels on or off and direct them to channels 0 and 1.

This method is demonstrated in the DVDSample application in <b>CKaraokeDlg::DoModal</b>.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>
              Annex J Command Name
            </td>
<td>
              Valid Domains
            </td>
</tr>
<tr>
<td>Karaoke_Audio_Presentation_Mode_Change</td>
<td>
<ul>
<li>DVD_DOMAIN_VideoManagerMenu</li>
<li>DVD_DOMAIN_VideoTitleSetMenu</li>
<li>DVD_DOMAIN_Title</li>
<li>DVD_DOMAIN_Stop</li>
</ul>
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/78b2998b-d8b3-424d-85bc-872e64eb4a4f">DVD Karaoke Property Set</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2 Interface</a>
 

 

