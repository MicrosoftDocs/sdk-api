---
UID: NF:strmif.IDvdControl2.SetOption
title: IDvdControl2::SetOption (strmif.h)
description: The SetOption method enables or disables an internal behavior flag on the DVD Navigator filter.
helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","SetOption method","IDvdControl2.SetOption","IDvdControl2::SetOption","IDvdControl2SetOption","SetOption","SetOption method [DirectShow]","SetOption method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_setoption","strmif/IDvdControl2::SetOption"]
old-location: dshow\idvdcontrol2_setoption.htm
tech.root: dshow
ms.assetid: b3b28da8-b0cb-4d76-8184-93572e4b6d06
ms.date: 4/26/2023
ms.keywords: IDvdControl2 interface [DirectShow],SetOption method, IDvdControl2.SetOption, IDvdControl2::SetOption, IDvdControl2SetOption, SetOption, SetOption method [DirectShow], SetOption method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_setoption, strmif/IDvdControl2::SetOption
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
 - IDvdControl2::SetOption
 - strmif/IDvdControl2::SetOption
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
 - IDvdControl2.SetOption
---

# IDvdControl2::SetOption


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetOption</b> method enables or disables an internal behavior flag on the <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> filter.

## -parameters

### -param flag [in]

Specifies which behavior to modify, as a member of the [DVD_OPTION_FLAG](/windows/desktop/api/strmif/ne-strmif-dvd_option_flag) enumeration type.

### -param fState [in]

Specifies the new value of the option given in the <i>flag</i> parameter.

[DVD_OPTION_FLAG](/windows/desktop/api/strmif/ne-strmif-dvd_option_flag) reference page.
          </div>
<div> </div>

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid flag.

</td>
</tr>
</table>

## -remarks

Call <b>SetOption</b> with the desired flags immediately after creating an instance of the DVD Navigator and whenever you want to change any behaviors.
      

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.
      

<table>
<tr>
<th>Annex J Command Name
            </th>
<th>Valid Domains
            </th>
</tr>
<tr>
<td>None</td>
<td>All</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>