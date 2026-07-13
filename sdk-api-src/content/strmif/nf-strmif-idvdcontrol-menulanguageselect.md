---
UID: NF:strmif.IDvdControl.MenuLanguageSelect
title: IDvdControl::MenuLanguageSelect (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Sets the displayed language for navigation menus.
helpviewer_keywords: ["IDvdControl interface [DirectShow]","MenuLanguageSelect method","IDvdControl.MenuLanguageSelect","IDvdControl::MenuLanguageSelect","IDvdControlMenuLanguageSelect","MenuLanguageSelect","MenuLanguageSelect method [DirectShow]","MenuLanguageSelect method [DirectShow]","IDvdControl interface","dshow.idvdcontrol_menulanguageselect","strmif/IDvdControl::MenuLanguageSelect"]
old-location: dshow\idvdcontrol_menulanguageselect.htm
tech.root: dshow
ms.assetid: 6b5c660c-3d3f-4f78-8eca-3a42982eb0ae
ms.date: 4/26/2023
ms.keywords: IDvdControl interface [DirectShow],MenuLanguageSelect method, IDvdControl.MenuLanguageSelect, IDvdControl::MenuLanguageSelect, IDvdControlMenuLanguageSelect, MenuLanguageSelect, MenuLanguageSelect method [DirectShow], MenuLanguageSelect method [DirectShow],IDvdControl interface, dshow.idvdcontrol_menulanguageselect, strmif/IDvdControl::MenuLanguageSelect
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
 - IDvdControl::MenuLanguageSelect
 - strmif/IDvdControl::MenuLanguageSelect
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
 - IDvdControl.MenuLanguageSelect
---

# IDvdControl::MenuLanguageSelect


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Sets the displayed language for navigation menus.

## -parameters

### -param Language

Value that specifies the new language.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method selects the default language for menus.

This method returns an error unless the domain is DVD_DOMAIN_Stop. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

Applications specify languages with standard Windows LCIDs.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>