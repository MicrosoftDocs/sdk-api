---
UID: NS:strmif.REGPINTYPES
title: REGPINTYPES (strmif.h)
description: The REGPINTYPES structure contains media type information for registering a filter.
helpviewer_keywords: ["AMOVIESETUP_MEDIATYPE","AMOVIESETUP_MEDIATYPE structure [DirectShow]","LPAMOVIESETUP_MEDIATYPE","LPAMOVIESETUP_MEDIATYPE structure pointer [DirectShow]","PAMOVIESETUP_MEDIATYPE","PAMOVIESETUP_MEDIATYPE structure pointer [DirectShow]","REGPINTYPES","REGPINTYPES structure [DirectShow]","REGPINTYPESStructure","dshow.regpintypes","strmif/AMOVIESETUP_MEDIATYPE","strmif/LPAMOVIESETUP_MEDIATYPE","strmif/PAMOVIESETUP_MEDIATYPE","strmif/REGPINTYPES"]
old-location: dshow\regpintypes.htm
tech.root: dshow
ms.assetid: aa31f856-4151-420d-a69d-34ef3a105130
ms.date: 12/05/2018
ms.keywords: AMOVIESETUP_MEDIATYPE, AMOVIESETUP_MEDIATYPE structure [DirectShow], LPAMOVIESETUP_MEDIATYPE, LPAMOVIESETUP_MEDIATYPE structure pointer [DirectShow], PAMOVIESETUP_MEDIATYPE, PAMOVIESETUP_MEDIATYPE structure pointer [DirectShow], REGPINTYPES, REGPINTYPES structure [DirectShow], REGPINTYPESStructure, dshow.regpintypes, strmif/AMOVIESETUP_MEDIATYPE, strmif/LPAMOVIESETUP_MEDIATYPE, strmif/PAMOVIESETUP_MEDIATYPE, strmif/REGPINTYPES
f1_keywords:
- strmif/REGPINTYPES
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- strmif.h
api_name:
- REGPINTYPES
targetos: Windows
req.typenames: REGPINTYPES
req.redist: 
ms.custom: 19H1
---

# REGPINTYPES structure


## -description



The <code>REGPINTYPES</code> structure contains media type information for registering a filter.




## -struct-fields




### -field clsMajorType

Major type GUID of the media type.


### -field clsMinorType

Sub type GUID of the media type. Can be MEDIASUBTYPE_NULL.


## -remarks



This structure is used by the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifiltermapper2">IFilterMapper2</a> interface to identify the media types that a pin supports. The equivalent <b>AMOVIESETUP_MEDIATYPE</b> type is used in class factory templates (<a href="https://docs.microsoft.com/windows/desktop/DirectShow/cfactorytemplate">CFactoryTemplate</a>).

To register a range of subtypes within the same major type, use the value MEDIASUBTYPE_NULL.

For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/how-to-register-directshow-filters">How to Register DirectShow Filters</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/media-types">Media Types</a>
 

 

