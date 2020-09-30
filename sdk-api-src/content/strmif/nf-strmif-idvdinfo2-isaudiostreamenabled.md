---
UID: NF:strmif.IDvdInfo2.IsAudioStreamEnabled
title: IDvdInfo2::IsAudioStreamEnabled (strmif.h)
description: The IsAudioStreamEnabled method determines if the specified audio stream is enabled in the current title.
helpviewer_keywords: ["IDvdInfo2 interface [DirectShow]","IsAudioStreamEnabled method","IDvdInfo2.IsAudioStreamEnabled","IDvdInfo2::IsAudioStreamEnabled","IDvdInfo2IsAudioStreamEnabled","IsAudioStreamEnabled","IsAudioStreamEnabled method [DirectShow]","IsAudioStreamEnabled method [DirectShow]","IDvdInfo2 interface","dshow.idvdinfo2_isaudiostreamenabled","strmif/IDvdInfo2::IsAudioStreamEnabled"]
old-location: dshow\idvdinfo2_isaudiostreamenabled.htm
tech.root: dshow
ms.assetid: 34938f9b-d3d8-4f38-95b4-bd65a5e88458
ms.date: 12/05/2018
ms.keywords: IDvdInfo2 interface [DirectShow],IsAudioStreamEnabled method, IDvdInfo2.IsAudioStreamEnabled, IDvdInfo2::IsAudioStreamEnabled, IDvdInfo2IsAudioStreamEnabled, IsAudioStreamEnabled, IsAudioStreamEnabled method [DirectShow], IsAudioStreamEnabled method [DirectShow],IDvdInfo2 interface, dshow.idvdinfo2_isaudiostreamenabled, strmif/IDvdInfo2::IsAudioStreamEnabled
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
 - IDvdInfo2::IsAudioStreamEnabled
 - strmif/IDvdInfo2::IsAudioStreamEnabled
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
 - IDvdInfo2.IsAudioStreamEnabled
---

# IDvdInfo2::IsAudioStreamEnabled


## -description

The <code>IsAudioStreamEnabled</code> method determines if the specified audio stream is enabled in the current title.

## -parameters

### -param ulStreamNum [in]

Audio stream number to test.

### -param pbEnabled [out]

Pointer to a variable of type BOOL that receives a value of <b>TRUE</b> if the audio stream is enabled, or <b>FALSE</b> otherwise.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> is not initialized.

</td>
</tr>
</table>

## -remarks

A DVD can have up to eight separate audio streams, although typically not all the streams will be enabled for each title. Use <code>IsAudioStreamEnabled</code> to determine whether a particular stream is enabled for the current title, and then call <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectaudiostream">IDvdControl2::SelectAudioStream</a> to select one of the enabled streams.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>