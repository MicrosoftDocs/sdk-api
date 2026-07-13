---
UID: NF:strmif.IDvdControl.ButtonSelectAndActivate
title: IDvdControl::ButtonSelectAndActivate (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Selects and activates the specified button.
helpviewer_keywords: ["ButtonSelectAndActivate","ButtonSelectAndActivate method [DirectShow]","ButtonSelectAndActivate method [DirectShow]","IDvdControl interface","IDvdControl interface [DirectShow]","ButtonSelectAndActivate method","IDvdControl.ButtonSelectAndActivate","IDvdControl::ButtonSelectAndActivate","IDvdControlButtonSelectAndActivate","dshow.idvdcontrol_buttonselectandactivate","strmif/IDvdControl::ButtonSelectAndActivate"]
old-location: dshow\idvdcontrol_buttonselectandactivate.htm
tech.root: dshow
ms.assetid: 15ed6a4e-d798-49c9-bff3-c77207658d31
ms.date: 4/26/2023
ms.keywords: ButtonSelectAndActivate, ButtonSelectAndActivate method [DirectShow], ButtonSelectAndActivate method [DirectShow],IDvdControl interface, IDvdControl interface [DirectShow],ButtonSelectAndActivate method, IDvdControl.ButtonSelectAndActivate, IDvdControl::ButtonSelectAndActivate, IDvdControlButtonSelectAndActivate, dshow.idvdcontrol_buttonselectandactivate, strmif/IDvdControl::ButtonSelectAndActivate
req.header: strmif.h
req.include-header: Dshow.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvdControl::ButtonSelectAndActivate
 - strmif/IDvdControl::ButtonSelectAndActivate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IDvdControl.ButtonSelectAndActivate
---

# IDvdControl::ButtonSelectAndActivate


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Selects and activates the specified button.

## -parameters

### -param ulButton [in]

Value that specifies the button that will be selected and activated, which must be from 1 through 36.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

Electronic remote control devices typically have a number of buttons that activate various functions of a DVD playback unit. Typically, you call this method when a user clicks a button on the control device; DirectShow then indicates that the button was selected (by playing a sound or changing a graphic, for example) and calls methods appropriate to which button was selected, such as <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-buttonactivate">ButtonActivate</a>.

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, or DVD_DOMAIN_Title. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>