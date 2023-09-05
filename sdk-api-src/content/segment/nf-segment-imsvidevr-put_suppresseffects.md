---
UID: NF:segment.IMSVidEVR.put_SuppressEffects
title: IMSVidEVR::put_SuppressEffects (segment.h)
description: The put_SuppressEffects method specifies whether the Video Control configures the system for optimal video playback.
helpviewer_keywords: ["IMSVidEVR interface [Microsoft TV Technologies]","put_SuppressEffects method","IMSVidEVR.put_SuppressEffects","IMSVidEVR::put_SuppressEffects","IMSVidEVRput_SuppressEffects","mstv.imsvidevr_put_suppresseffects","put_SuppressEffects","put_SuppressEffects method [Microsoft TV Technologies]","put_SuppressEffects method [Microsoft TV Technologies]","IMSVidEVR interface","segment/IMSVidEVR::put_SuppressEffects"]
old-location: mstv\imsvidevr_put_suppresseffects.htm
tech.root: mstv
ms.assetid: 399250b6-4f2d-4dbf-b1e8-d32a0673617e
ms.date: 12/05/2018
ms.keywords: IMSVidEVR interface [Microsoft TV Technologies],put_SuppressEffects method, IMSVidEVR.put_SuppressEffects, IMSVidEVR::put_SuppressEffects, IMSVidEVRput_SuppressEffects, mstv.imsvidevr_put_suppresseffects, put_SuppressEffects, put_SuppressEffects method [Microsoft TV Technologies], put_SuppressEffects method [Microsoft TV Technologies],IMSVidEVR interface, segment/IMSVidEVR::put_SuppressEffects
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - IMSVidEVR::put_SuppressEffects
 - segment/IMSVidEVR::put_SuppressEffects
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidEVR.put_SuppressEffects
---

# IMSVidEVR::put_SuppressEffects


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_SuppressEffects</b> method specifies whether the <a href="/previous-versions/windows/desktop/legacy/ee663618(v=vs.85)">Video Control</a> configures the system for optimal video playback.

## -parameters

### -param bSuppress [in]

Specifies a Boolean value. See Remarks for more information.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

If <i>bSuppress</i> equals VARIANT_TRUE, the Video Control configures several system parameters during video playback:

<ul>
<li>Disables the screen saver timeout.</li>
<li>Disables Microsoft ClearType smoothing.</li>
<li>Disables the drop shadow effect.</li>
<li>Disables alpha-blended mouse cursors.</li>
<li>Prevents the system from turning off the display (power management).</li>
</ul>
For applications based on the Windows Graphics Device Interface (GDI), these settings improve the video playback experience. When playback stops, the Video Control restores the original system settings.

If <i>bSuppress</i> equals VARIANT_FALSE, the Video Control does not modify any of these system settings.

The default value for this property is VARIANT_TRUE. Set this property to VARIANT_FALSE if your application wants to control all of the system settings; for example, if you are providing a custom presenter.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidevr">IMSVidEVR</a>