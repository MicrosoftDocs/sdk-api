---
UID: NE:strmif.tagDVD_NavCmdType
title: DVD_NavCmdType (strmif.h)
description: Defines DVD navigation command types.
helpviewer_keywords: ["DVD_NavCmdType","DVD_NavCmdType enumeration [DirectShow]","DVD_NavCmdType_Button","DVD_NavCmdType_Cell","DVD_NavCmdType_Post","DVD_NavCmdType_Pre","dshow.dvd_navcmdtype","strmif/DVD_NavCmdType","strmif/DVD_NavCmdType_Button","strmif/DVD_NavCmdType_Cell","strmif/DVD_NavCmdType_Post","strmif/DVD_NavCmdType_Pre"]
old-location: dshow\dvd_navcmdtype.htm
tech.root: dshow
ms.assetid: cefe9a5f-3cd6-4b4c-96d5-cd4746a80729
ms.date: 4/26/2023
ms.keywords: DVD_NavCmdType, DVD_NavCmdType enumeration [DirectShow], DVD_NavCmdType_Button, DVD_NavCmdType_Cell, DVD_NavCmdType_Post, DVD_NavCmdType_Pre, dshow.dvd_navcmdtype, strmif/DVD_NavCmdType, strmif/DVD_NavCmdType_Button, strmif/DVD_NavCmdType_Cell, strmif/DVD_NavCmdType_Post, strmif/DVD_NavCmdType_Pre
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
req.typenames: DVD_NavCmdType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDVD_NavCmdType
 - strmif/tagDVD_NavCmdType
 - DVD_NavCmdType
 - strmif/DVD_NavCmdType
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
 - DVD_NavCmdType
---

# DVD_NavCmdType enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Defines DVD navigation command types.

## -enum-fields

### -field DVD_NavCmdType_Pre:1

Pre-command.

### -field DVD_NavCmdType_Post:2

Post-command.

### -field DVD_NavCmdType_Cell:3

Cell command.

### -field DVD_NavCmdType_Button:4

Button command.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/DirectShow/ec-dvd-beginnavigationcommands">EC_DVD_BeginNavigationCommands</a>
