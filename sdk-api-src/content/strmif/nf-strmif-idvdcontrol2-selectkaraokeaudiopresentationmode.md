---
UID: NF:strmif.IDvdControl2.SelectKaraokeAudioPresentationMode
title: IDvdControl2::SelectKaraokeAudioPresentationMode (strmif.h)
description: The SelectKaraokeAudioPresentationMode method sends karaoke auxiliary channels to the left or right speakers.helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","SelectKaraokeAudioPresentationMode method","IDvdControl2.SelectKaraokeAudioPresentationMode","IDvdControl2::SelectKaraokeAudioPresentationMode","IDvdControl2SelectKaraokeAudioPresentationMode","SelectKaraokeAudioPresentationMode","SelectKaraokeAudioPresentationMode method [DirectShow]","SelectKaraokeAudioPresentationMode method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_selectkaraokeaudiopresentationmode","strmif/IDvdControl2::SelectKaraokeAudioPresentationMode"]
old-location: dshow\idvdcontrol2_selectkaraokeaudiopresentationmode.htm
tech.root: DirectShow
ms.assetid: 9101fd83-1349-4cdd-b5e9-6daeb7d1e3d8
ms.date: 12/05/2018
ms.keywords: IDvdControl2 interface [DirectShow],SelectKaraokeAudioPresentationMode method, IDvdControl2.SelectKaraokeAudioPresentationMode, IDvdControl2::SelectKaraokeAudioPresentationMode, IDvdControl2SelectKaraokeAudioPresentationMode, SelectKaraokeAudioPresentationMode, SelectKaraokeAudioPresentationMode method [DirectShow], SelectKaraokeAudioPresentationMode method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_selectkaraokeaudiopresentationmode, strmif/IDvdControl2::SelectKaraokeAudioPresentationMode
f1_keywords:
- strmif/IDvdControl2.SelectKaraokeAudioPresentationMode
dev_langs:
- c++
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IDvdControl2.SelectKaraokeAudioPresentationMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl2::SelectKaraokeAudioPresentationMode


## -description



The <code>SelectKaraokeAudioPresentationMode</code> method sends karaoke auxiliary channels to the left or right speakers.




## -parameters




### -param ulMode [in]

Bitwise OR of [DVD_KARAOKE_DOWNMIX](https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_karaoke_downmix) enumeration indicating how to downmix the five karaoke channels to channels 0 and 1, which are usually output to the left and right speakers.


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
The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> filter is in an invalid domain.

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
<td>Annex J Command Name
            </td>
<td>Valid Domains
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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-karaoke-property-set">DVD Karaoke Property Set</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>
 

 

