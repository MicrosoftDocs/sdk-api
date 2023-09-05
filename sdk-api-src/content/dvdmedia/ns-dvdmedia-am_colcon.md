---
UID: NS:dvdmedia._AM_COLCON
title: AM_COLCON (dvdmedia.h)
description: Indicates the color contrast description from the DVD highlight (HLI) structure.
helpviewer_keywords: ["*PAM_COLCON","AM_COLCON","AM_COLCON structure [DirectShow]","PAM_COLCON","PAM_COLCON structure pointer [DirectShow]","dshow.am_colcon","dvdmedia/AM_COLCON","dvdmedia/PAM_COLCON"]
old-location: dshow\am_colcon.htm
tech.root: dshow
ms.assetid: 9358d860-6187-48d9-81b6-d5d65d73786d
ms.date: 4/26/2023
ms.keywords: '*PAM_COLCON, AM_COLCON, AM_COLCON structure [DirectShow], PAM_COLCON, PAM_COLCON structure pointer [DirectShow], dshow.am_colcon, dvdmedia/AM_COLCON, dvdmedia/PAM_COLCON'
req.header: dvdmedia.h
req.include-header: 
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
req.typenames: AM_COLCON, *PAM_COLCON
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AM_COLCON
 - dvdmedia/_AM_COLCON
 - PAM_COLCON
 - dvdmedia/PAM_COLCON
 - AM_COLCON
 - dvdmedia/AM_COLCON
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dvdmedia.h
api_name:
 - AM_COLCON
---

# AM_COLCON structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Indicates the color contrast description from the DVD highlight (HLI) structure.

## -struct-fields

### -field emph1col

Emphasis color 1.

### -field emph2col

Emphasis color 2.

### -field backcol

Background color.

### -field patcol

Pattern color.

### -field emph1con

Emphasis contrast 1.

### -field emph2con

Emphasis contrast 2.

### -field backcon

Background contrast.

### -field patcon

Pattern contrast.

## -remarks

This structure is contained within the <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_property_sphli">AM_PROPERTY_SPHLI</a> structure.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-subpicture-property-set">DVD Subpicture Property Set</a>