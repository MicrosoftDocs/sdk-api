---
UID: NF:strmif.IDvdInfo2.GetAllGPRMs
title: IDvdInfo2::GetAllGPRMs (strmif.h)
description: The GetAllGPRMs method retrieves the current contents of all general parameter registers (GPRMs).
helpviewer_keywords: ["GetAllGPRMs","GetAllGPRMs method [DirectShow]","GetAllGPRMs method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetAllGPRMs method","IDvdInfo2.GetAllGPRMs","IDvdInfo2::GetAllGPRMs","IDvdInfo2GetAllGPRMs","dshow.idvdinfo2_getallgprms","strmif/IDvdInfo2::GetAllGPRMs"]
old-location: dshow\idvdinfo2_getallgprms.htm
tech.root: dshow
ms.assetid: 994f57b5-8514-4768-a679-21133ec92e32
ms.date: 4/26/2023
ms.keywords: GetAllGPRMs, GetAllGPRMs method [DirectShow], GetAllGPRMs method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetAllGPRMs method, IDvdInfo2.GetAllGPRMs, IDvdInfo2::GetAllGPRMs, IDvdInfo2GetAllGPRMs, dshow.idvdinfo2_getallgprms, strmif/IDvdInfo2::GetAllGPRMs
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvdInfo2::GetAllGPRMs
 - strmif/IDvdInfo2::GetAllGPRMs
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
 - IDvdInfo2.GetAllGPRMs
---

# IDvdInfo2::GetAllGPRMs


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetAllGPRMs</b> method retrieves the current contents of all general parameter registers (GPRMs).

## -parameters

### -param pRegisterArray [out]

Pointer to an array of type <a href="/windows/desktop/DirectShow/gprmarray">GPRMARRAY</a> that receives all 16 current GPRM values.

## -returns

Returns one of the following <b>HRESULT</b> values.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
</table>

## -remarks

GPRMs are 16-bit registers that each disc can use in unique ways for temporary data storage. 

<div class="alert"><b>Note</b>  A player application using the <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> filter does not need to access these registers for any Annex J playback or navigation control. This method is provided for player applications implementing advanced functionality. Do not attempt to modify the GPRMs directly unless you have a thorough knowledge of the DVD specification, and the ways in which the GPRMs are used on the particular discs to be played.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>