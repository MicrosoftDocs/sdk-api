---
UID: NF:strmif.IDvdControl2.SelectAndActivateButton
title: IDvdControl2::SelectAndActivateButton (strmif.h)
description: The SelectAndActivateButton method selects and activates the specified menu button.
helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","SelectAndActivateButton method","IDvdControl2.SelectAndActivateButton","IDvdControl2::SelectAndActivateButton","IDvdControl2SelectAndActivateButton","SelectAndActivateButton","SelectAndActivateButton method [DirectShow]","SelectAndActivateButton method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_selectandactivatebutton","strmif/IDvdControl2::SelectAndActivateButton"]
old-location: dshow\idvdcontrol2_selectandactivatebutton.htm
tech.root: dshow
ms.assetid: 1e5ad753-bc35-4a98-83d8-82ffccbbe3ed
ms.date: 4/26/2023
ms.keywords: IDvdControl2 interface [DirectShow],SelectAndActivateButton method, IDvdControl2.SelectAndActivateButton, IDvdControl2::SelectAndActivateButton, IDvdControl2SelectAndActivateButton, SelectAndActivateButton, SelectAndActivateButton method [DirectShow], SelectAndActivateButton method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_selectandactivatebutton, strmif/IDvdControl2::SelectAndActivateButton
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
 - IDvdControl2::SelectAndActivateButton
 - strmif/IDvdControl2::SelectAndActivateButton
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
 - IDvdControl2.SelectAndActivateButton
---

# IDvdControl2::SelectAndActivateButton


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SelectAndActivateButton</code> method selects and activates the specified menu button.

## -parameters

### -param ulButton [in]

Value from 1 through 36 that specifies the button to select and activate.

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
<i>ulButton</i> is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The <i>ulButton</i> value is valid, but the <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> filter couldn't activate it.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
UOP control prohibits the operation.

</td>
</tr>
</table>

## -remarks

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>Button_Select_and_Activate</td>
<td>
<ul>
<li>DVD_DOMAIN_VideoManagerMenu</li>
<li>DVD_DOMAIN_VideoTitleSetMenu</li>
<li>DVD_DOMAIN_Title</li>
</ul>
</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>



<a href="/windows/desktop/DirectShow/working-with-dvd-menus">Working With DVD Menus</a>