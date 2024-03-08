---
UID: NF:strmif.IAMPhysicalPinInfo.GetPhysicalType
title: IAMPhysicalPinInfo::GetPhysicalType (strmif.h)
description: Note  The IAMPhysicalPinInfo interface is deprecated. Retrieves the type and name of the physical pin.
helpviewer_keywords: ["GetPhysicalType","GetPhysicalType method [DirectShow]","GetPhysicalType method [DirectShow]","IAMPhysicalPinInfo interface","IAMPhysicalPinInfo interface [DirectShow]","GetPhysicalType method","IAMPhysicalPinInfo.GetPhysicalType","IAMPhysicalPinInfo::GetPhysicalType","IAMPhysicalPinInfoGetPhysicalType","dshow.iamphysicalpininfo_getphysicaltype","strmif/IAMPhysicalPinInfo::GetPhysicalType"]
old-location: dshow\iamphysicalpininfo_getphysicaltype.htm
tech.root: dshow
ms.assetid: e18be591-64c7-4da0-aa28-c51dca7901b7
ms.date: 4/26/2023
ms.keywords: GetPhysicalType, GetPhysicalType method [DirectShow], GetPhysicalType method [DirectShow],IAMPhysicalPinInfo interface, IAMPhysicalPinInfo interface [DirectShow],GetPhysicalType method, IAMPhysicalPinInfo.GetPhysicalType, IAMPhysicalPinInfo::GetPhysicalType, IAMPhysicalPinInfoGetPhysicalType, dshow.iamphysicalpininfo_getphysicaltype, strmif/IAMPhysicalPinInfo::GetPhysicalType
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMPhysicalPinInfo::GetPhysicalType
 - strmif/IAMPhysicalPinInfo::GetPhysicalType
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
 - IAMPhysicalPinInfo.GetPhysicalType
---

# IAMPhysicalPinInfo::GetPhysicalType


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <code>IAMPhysicalPinInfo</code> interface is deprecated.</div>
<div> </div>
Retrieves the type and name of the physical pin.

## -parameters

### -param pType [out]

Pointer to a variable that receives a value indicating the pin's type. The [PhysicalConnectorType](/windows/desktop/api/strmif/ne-strmif-physicalconnectortype) enumeration defines the pin type values.

### -param ppszType [out]

Address of a pointer to a buffer that receives a human-readable string identifying the pin type.

## -returns

Returns S_OK if a valid physical pin value is found. Otherwise, returns VFW_E_NO_ACCEPTABLE_TYPES.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamphysicalpininfo">IAMPhysicalPinInfo Interface</a>