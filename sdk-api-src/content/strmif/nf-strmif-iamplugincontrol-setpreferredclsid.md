---
UID: NF:strmif.IAMPluginControl.SetPreferredClsid
title: IAMPluginControl::SetPreferredClsid (strmif.h)
description: Adds a class identifier (CLSID) to the preferred list or removes a CLSID from the list. (IAMPluginControl.SetPreferredClsid)
helpviewer_keywords: ["IAMPluginControl interface [DirectShow]","SetPreferredClsid method","IAMPluginControl.SetPreferredClsid","IAMPluginControl::SetPreferredClsid","SetPreferredClsid","SetPreferredClsid method [DirectShow]","SetPreferredClsid method [DirectShow]","IAMPluginControl interface","dshow.iamplugincontrol_setpreferredclsid","strmif/IAMPluginControl::SetPreferredClsid"]
old-location: dshow\iamplugincontrol_setpreferredclsid.htm
tech.root: dshow
ms.assetid: 45702714-6b35-4863-885e-55049258a4ae
ms.date: 4/26/2023
ms.keywords: IAMPluginControl interface [DirectShow],SetPreferredClsid method, IAMPluginControl.SetPreferredClsid, IAMPluginControl::SetPreferredClsid, SetPreferredClsid, SetPreferredClsid method [DirectShow], SetPreferredClsid method [DirectShow],IAMPluginControl interface, dshow.iamplugincontrol_setpreferredclsid, strmif/IAMPluginControl::SetPreferredClsid
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Axextend.idl
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
 - IAMPluginControl::SetPreferredClsid
 - strmif/IAMPluginControl::SetPreferredClsid
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
 - IAMPluginControl.SetPreferredClsid
---

# IAMPluginControl::SetPreferredClsid


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Adds a class identifier (CLSID) to the preferred list or removes a CLSID from the list.

## -parameters

### -param subType [in]

A media subtype GUID to associate with the CLSID.

### -param clsid [in]

Pointer to the CLSID to add to the list. If this parameter is <b>NULL</b>, the entry associated with <i>subType</i> is removed from the list

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-iamplugincontrol">IAMPluginControl</a>



<a href="/windows/desktop/DirectShow/intelligent-connect">Intelligent Connect</a>
