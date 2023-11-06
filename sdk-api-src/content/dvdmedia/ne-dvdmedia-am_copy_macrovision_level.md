---
UID: NE:dvdmedia.AM_COPY_MACROVISION_LEVEL
title: AM_COPY_MACROVISION_LEVEL (dvdmedia.h)
description: Identifies the analog copy protection level.
helpviewer_keywords: ["*PAM_COPY_MACROVISION_LEVEL","AM_COPY_MACROVISION_LEVEL","AM_COPY_MACROVISION_LEVEL enumeration [DirectShow]","AM_MACROVISION_DISABLED","AM_MACROVISION_LEVEL1","AM_MACROVISION_LEVEL2","AM_MACROVISION_LEVEL3","PAM_COPY_MACROVISION_LEVEL","PAM_COPY_MACROVISION_LEVEL enumeration pointer [DirectShow]","dshow.am_copy_macrovision_level","dvdmedia/AM_COPY_MACROVISION_LEVEL","dvdmedia/AM_MACROVISION_DISABLED","dvdmedia/AM_MACROVISION_LEVEL1","dvdmedia/AM_MACROVISION_LEVEL2","dvdmedia/AM_MACROVISION_LEVEL3","dvdmedia/PAM_COPY_MACROVISION_LEVEL"]
old-location: dshow\am_copy_macrovision_level.htm
tech.root: dshow
ms.assetid: d71f78f4-1107-46ba-afa8-7de87e20d814
ms.date: 4/26/2023
ms.keywords: '*PAM_COPY_MACROVISION_LEVEL, AM_COPY_MACROVISION_LEVEL, AM_COPY_MACROVISION_LEVEL enumeration [DirectShow], AM_MACROVISION_DISABLED, AM_MACROVISION_LEVEL1, AM_MACROVISION_LEVEL2, AM_MACROVISION_LEVEL3, PAM_COPY_MACROVISION_LEVEL, PAM_COPY_MACROVISION_LEVEL enumeration pointer [DirectShow], dshow.am_copy_macrovision_level, dvdmedia/AM_COPY_MACROVISION_LEVEL, dvdmedia/AM_MACROVISION_DISABLED, dvdmedia/AM_MACROVISION_LEVEL1, dvdmedia/AM_MACROVISION_LEVEL2, dvdmedia/AM_MACROVISION_LEVEL3, dvdmedia/PAM_COPY_MACROVISION_LEVEL'
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
req.typenames: AM_COPY_MACROVISION_LEVEL, *PAM_COPY_MACROVISION_LEVEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PAM_COPY_MACROVISION_LEVEL
 - dvdmedia/PAM_COPY_MACROVISION_LEVEL
 - AM_COPY_MACROVISION_LEVEL
 - dvdmedia/AM_COPY_MACROVISION_LEVEL
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
 - AM_COPY_MACROVISION_LEVEL
---

# AM_COPY_MACROVISION_LEVEL enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Identifies the analog copy protection level.

## -enum-fields

### -field AM_MACROVISION_DISABLED:0

Disabled.

### -field AM_MACROVISION_LEVEL1:1

Level 1.

### -field AM_MACROVISION_LEVEL2:2

Level 2.

### -field AM_MACROVISION_LEVEL3:3

Level 3.

## -remarks

The <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_copy_macrovision">AM_COPY_MACROVISION</a> structure uses this data type.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-copy-protection-property-set">DVD Copy Protection Property Set</a>

