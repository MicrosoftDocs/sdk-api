---
UID: NE:evr._EVRFilterConfig_Prefs
title: EVRFilterConfigPrefs (evr.h)
description: Contains flags that are used to configure the Microsoft DirectShow enhanced video renderer (EVR) filter.
helpviewer_keywords: ["EVRFilterConfigPrefs","EVRFilterConfigPrefs enumeration [Media Foundation]","EVRFilterConfigPrefs_EnableQoS","EVRFilterConfigPrefs_Mask","evr/EVRFilterConfigPrefs","evr/EVRFilterConfigPrefs_EnableQoS","evr/EVRFilterConfigPrefs_Mask","mf.evrfilterconfigprefs"]
old-location: mf\evrfilterconfigprefs.htm
tech.root: mfarchive
ms.assetid: 39d6845e-8655-4f8f-be39-76d704fd1177
ms.date: 12/05/2018
ms.keywords: EVRFilterConfigPrefs, EVRFilterConfigPrefs enumeration [Media Foundation], EVRFilterConfigPrefs_EnableQoS, EVRFilterConfigPrefs_Mask, evr/EVRFilterConfigPrefs, evr/EVRFilterConfigPrefs_EnableQoS, evr/EVRFilterConfigPrefs_Mask, mf.evrfilterconfigprefs
req.header: evr.h
req.include-header: 
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
req.typenames: EVRFilterConfigPrefs
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVRFilterConfig_Prefs
 - evr/_EVRFilterConfig_Prefs
 - EVRFilterConfigPrefs
 - evr/EVRFilterConfigPrefs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - evr.h
api_name:
 - EVRFilterConfigPrefs
archived: true
---

# EVRFilterConfigPrefs enumeration


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Contains flags that are used to configure the Microsoft DirectShow enhanced video renderer (EVR) filter.

## -enum-fields

### -field EVRFilterConfigPrefs_EnableQoS:0x1

Enables dynamic adjustments to video quality during playback.

### -field EVRFilterConfigPrefs_Mask:0x1

The bitmask of valid flag values. This constant is not itself a valid flag.

## -see-also

<a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfigex">IEVRFilterConfigEx</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="/windows/desktop/medfound/video-quality-management">Video Quality Management</a>
