---
UID: NE:strmif.VfwCompressDialogs
title: VfwCompressDialogs (strmif.h)
description: Specifies a dialog box that might exist in a Video for Windows compression (codec) driver.
helpviewer_keywords: ["VfwCompressDialog_About","VfwCompressDialog_Config","VfwCompressDialog_QueryAbout","VfwCompressDialog_QueryConfig","VfwCompressDialogs","VfwCompressDialogs enumeration [DirectShow]","VfwCompressDialogsEnumeration","dshow.vfwcompressdialogs","strmif/VfwCompressDialog_About","strmif/VfwCompressDialog_Config","strmif/VfwCompressDialog_QueryAbout","strmif/VfwCompressDialog_QueryConfig","strmif/VfwCompressDialogs"]
old-location: dshow\vfwcompressdialogs.htm
tech.root: dshow
ms.assetid: b1e92603-631a-45e0-aee0-3974e3114e03
ms.date: 4/26/2023
ms.keywords: VfwCompressDialog_About, VfwCompressDialog_Config, VfwCompressDialog_QueryAbout, VfwCompressDialog_QueryConfig, VfwCompressDialogs, VfwCompressDialogs enumeration [DirectShow], VfwCompressDialogsEnumeration, dshow.vfwcompressdialogs, strmif/VfwCompressDialog_About, strmif/VfwCompressDialog_Config, strmif/VfwCompressDialog_QueryAbout, strmif/VfwCompressDialog_QueryConfig, strmif/VfwCompressDialogs
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
req.typenames: VfwCompressDialogs
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VfwCompressDialogs
 - strmif/VfwCompressDialogs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - VfwCompressDialogs
---

# VfwCompressDialogs enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies a dialog box that might exist in a Video for Windows compression (codec) driver.

## -enum-fields

### -field VfwCompressDialog_Config:0x1

Configure dialog box.

### -field VfwCompressDialog_About:0x2

About dialog box.

### -field VfwCompressDialog_QueryConfig:0x4

Specifies whether the Configure dialog box is available.

### -field VfwCompressDialog_QueryAbout:0x8

Specifies whether the About dialog box is available.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvfwcapturedialogs">IAMVfwCaptureDialogs Interface</a>
