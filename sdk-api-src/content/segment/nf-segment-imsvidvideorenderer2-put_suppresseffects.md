---
UID: NF:segment.IMSVidVideoRenderer2.put_SuppressEffects
title: IMSVidVideoRenderer2::put_SuppressEffects (segment.h)
description: The put_SuppressEffects method sets preferences for power management and visual effects.
helpviewer_keywords: ["IMSVidVideoRenderer2 interface [Microsoft TV Technologies]","put_SuppressEffects method","IMSVidVideoRenderer2.put_SuppressEffects","IMSVidVideoRenderer2::put_SuppressEffects","IMSVidVideoRenderer2put_SuppressEffects","mstv.imsvidvideorenderer2_put_suppresseffects","put_SuppressEffects","put_SuppressEffects method [Microsoft TV Technologies]","put_SuppressEffects method [Microsoft TV Technologies]","IMSVidVideoRenderer2 interface","segment/IMSVidVideoRenderer2::put_SuppressEffects"]
old-location: mstv\imsvidvideorenderer2_put_suppresseffects.htm
tech.root: mstv
ms.assetid: d362addb-626a-42f8-9b95-82189a338527
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer2 interface [Microsoft TV Technologies],put_SuppressEffects method, IMSVidVideoRenderer2.put_SuppressEffects, IMSVidVideoRenderer2::put_SuppressEffects, IMSVidVideoRenderer2put_SuppressEffects, mstv.imsvidvideorenderer2_put_suppresseffects, put_SuppressEffects, put_SuppressEffects method [Microsoft TV Technologies], put_SuppressEffects method [Microsoft TV Technologies],IMSVidVideoRenderer2 interface, segment/IMSVidVideoRenderer2::put_SuppressEffects
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IMSVidVideoRenderer2::put_SuppressEffects
 - segment/IMSVidVideoRenderer2::put_SuppressEffects
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
 - IMSVidVideoRenderer2.put_SuppressEffects
---

# IMSVidVideoRenderer2::put_SuppressEffects


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_SuppressEffects</b> method sets preferences for power management and visual effects.

## -parameters

### -param bSuppress [in]

Specifies a Boolean value. See Remarks for more information.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -remarks

If <i>bSuppress</i> equals VARIANT_TRUE, the Video Control does the following:

<ul>
<li>Disables font smoothing and the system-wide drop shadow effect. (Only when the Video Control is using hardware overlay.) This is useful if the application draws onto the overlay.</li>
<li>Disables the screen saver, and turns off power management for the display. This is useful to prevent the operating system from interrupting playback while the user is watching a program.</li>
</ul>
The Video Control restores the original system settings after it stops.

If <i>bSuppress</i> equals VARIANT_FALSE, the Video Control uses the existing system settings.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidvideorenderer2">IMSVidVideoRenderer2 Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_usingoverlay">IMSVidVideoRenderer::put_UsingOverlay</a>