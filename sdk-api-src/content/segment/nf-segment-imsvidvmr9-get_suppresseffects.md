---
UID: NF:segment.IMSVidVMR9.get_SuppressEffects
title: IMSVidVMR9::get_SuppressEffects (segment.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["IMSVidVMR9 interface [Microsoft TV Technologies]","get_SuppressEffects method","IMSVidVMR9.get_SuppressEffects","IMSVidVMR9::get_SuppressEffects","IMSVidVMR9get_SuppressEffects","get_SuppressEffects","get_SuppressEffects method [Microsoft TV Technologies]","get_SuppressEffects method [Microsoft TV Technologies]","IMSVidVMR9 interface","mstv.imsvidvmr9_get_suppresseffects","segment/IMSVidVMR9::get_SuppressEffects"]
old-location: mstv\imsvidvmr9_get_suppresseffects.htm
tech.root: mstv
ms.assetid: 7d2d10fe-39c2-4ee1-a5c5-5624b2fbc2ef
ms.date: 12/05/2018
ms.keywords: IMSVidVMR9 interface [Microsoft TV Technologies],get_SuppressEffects method, IMSVidVMR9.get_SuppressEffects, IMSVidVMR9::get_SuppressEffects, IMSVidVMR9get_SuppressEffects, get_SuppressEffects, get_SuppressEffects method [Microsoft TV Technologies], get_SuppressEffects method [Microsoft TV Technologies],IMSVidVMR9 interface, mstv.imsvidvmr9_get_suppresseffects, segment/IMSVidVMR9::get_SuppressEffects
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IMSVidVMR9::get_SuppressEffects
 - segment/IMSVidVMR9::get_SuppressEffects
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
 - IMSVidVMR9.get_SuppressEffects
---

# IMSVidVMR9::get_SuppressEffects


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>get_SuppressEffects</b> method queries whether the Video Control configures the system for optimal video playback.

## -parameters

### -param bSuppress [out]

Receives a <b>VARIANT_BOOL</b>. For more information, see <a href="/windows/desktop/api/segment/nf-segment-imsvidvmr9-put_suppresseffects">IMSVidVMR9::put_SuppressEffects</a>. The default value is VARIANT_TRUE.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvmr9">IMSVidVMR9 Interface</a>