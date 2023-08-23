---
UID: NF:strmif.IAMPluginControl.SetDisabled
title: IAMPluginControl::SetDisabled (strmif.h)
description: Adds a class identifier (CLSID) to the blocked list, or removes a CLSID from the list. (IAMPluginControl.SetDisabled)
helpviewer_keywords: ["IAMPluginControl interface [DirectShow]","SetDisabled method","IAMPluginControl.SetDisabled","IAMPluginControl::SetDisabled","SetDisabled","SetDisabled method [DirectShow]","SetDisabled method [DirectShow]","IAMPluginControl interface","dshow.iamplugincontrol_setdisabled","strmif/IAMPluginControl::SetDisabled"]
old-location: dshow\iamplugincontrol_setdisabled.htm
tech.root: dshow
ms.assetid: 3ac4b3b5-0882-4e30-b3fa-1dcee33a74d3
ms.date: 4/26/2023
ms.keywords: IAMPluginControl interface [DirectShow],SetDisabled method, IAMPluginControl.SetDisabled, IAMPluginControl::SetDisabled, SetDisabled, SetDisabled method [DirectShow], SetDisabled method [DirectShow],IAMPluginControl interface, dshow.iamplugincontrol_setdisabled, strmif/IAMPluginControl::SetDisabled
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IAMPluginControl::SetDisabled
 - strmif/IAMPluginControl::SetDisabled
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
 - IAMPluginControl.SetDisabled
---

# IAMPluginControl::SetDisabled


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Adds a class identifier (CLSID) to the blocked list, or removes a CLSID from the list.

## -parameters

### -param clsid [in]

The CLSID to add or remove.

### -param disabled [in]

Specifies whether to add or remove the CSLID. If the value is <b>TRUE</b>, the method adds the CLSID to the blocked list. Otherwise, the method removes it from the list.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-iamplugincontrol">IAMPluginControl</a>



<a href="/windows/desktop/DirectShow/intelligent-connect">Intelligent Connect</a>
