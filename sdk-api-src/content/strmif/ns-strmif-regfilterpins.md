---
UID: NS:strmif.REGFILTERPINS
title: REGFILTERPINS (strmif.h)
description: The REGFILTERPINS structure contains pin information for registering a filter.
helpviewer_keywords: ["AMOVIESETUP_PIN","AMOVIESETUP_PIN structure [DirectShow]","LPAMOVIESETUP_PIN","LPAMOVIESETUP_PIN structure pointer [DirectShow]","PAMOVIESETUP_PIN","PAMOVIESETUP_PIN structure pointer [DirectShow]","REGFILTERPINS","REGFILTERPINS structure [DirectShow]","REGFILTERPINSStructure","dshow.regfilterpins","strmif/AMOVIESETUP_PIN","strmif/LPAMOVIESETUP_PIN","strmif/PAMOVIESETUP_PIN","strmif/REGFILTERPINS"]
old-location: dshow\regfilterpins.htm
tech.root: dshow
ms.assetid: 1da033e1-24c3-46e0-becf-025966e6238f
ms.date: 4/26/2023
ms.keywords: AMOVIESETUP_PIN, AMOVIESETUP_PIN structure [DirectShow], LPAMOVIESETUP_PIN, LPAMOVIESETUP_PIN structure pointer [DirectShow], PAMOVIESETUP_PIN, PAMOVIESETUP_PIN structure pointer [DirectShow], REGFILTERPINS, REGFILTERPINS structure [DirectShow], REGFILTERPINSStructure, dshow.regfilterpins, strmif/AMOVIESETUP_PIN, strmif/LPAMOVIESETUP_PIN, strmif/PAMOVIESETUP_PIN, strmif/REGFILTERPINS
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
req.typenames: REGFILTERPINS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - REGFILTERPINS
 - strmif/REGFILTERPINS
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
 - REGFILTERPINS
---

# REGFILTERPINS structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>REGFILTERPINS</code> structure contains pin information for registering a filter.

## -struct-fields

### -field strName

Name of the pin. (Obsolete.)

### -field bRendered

If <b>TRUE</b>, the filter renders the input from this pin. (Applies only to input pins. For output pins, the value is always <b>FALSE</b>.)

### -field bOutput

If <b>TRUE</b>, this pin is an output pin. Otherwise, the pin is an input pin.

### -field bZero

If <b>TRUE</b>, the filter can have zero instances of this pin.

### -field bMany

If <b>TRUE</b>, the filter can create more than one instance of this type of pin.

### -field clsConnectsToFilter

Class identifier (CLSID) of the filter to which this pin connects. (Obsolete.)

### -field strConnectsToPin

Name of the pin to which this pin connects. (Obsolete.)

### -field nMediaTypes

Number of media types supported by this pin.

### -field lpMediaType

Pointer to an array of <a href="/windows/desktop/api/strmif/ns-strmif-regpintypes">REGPINTYPES</a> structures, of size <b>nMediaTypes</b>.

## -remarks

This structure is used in the <a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper2">IFilterMapper2</a> interface for filter registration. If you use this structure, set the <b>dwVersion</b> member of the <a href="/windows/desktop/api/strmif/ns-strmif-regfilter2">REGFILTER2</a> structure to 1. If you need to register a medium or pin category for the pin, use the <a href="/windows/desktop/api/strmif/ns-strmif-regfilterpins2">REGFILTERPINS2</a> structure instead. In that case, set the <b>REGFILTER2</b> structure's <b>dwVersion</b> member to 2.

The equivalent <b>AMOVIESETUP_PIN</b> type is used in class factory templates (<a href="/windows/desktop/DirectShow/cfactorytemplate">CFactoryTemplate</a>).

The <b>strName</b>, <b>clsConnectsToFilter</b>, and <b>strConnectsToPin</b> members are obsolete. Their values are not added to the registry.

For more information, see <a href="/windows/desktop/DirectShow/how-to-register-directshow-filters">How to Register DirectShow Filters</a>.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>