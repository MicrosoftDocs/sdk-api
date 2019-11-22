---
UID: NE:strmif._AM_PUSHSOURCE_FLAGS
title: "_AM_PUSHSOURCE_FLAGS" (strmif.h)

description: Indicates the behavior of a live source filter.
old-location: dshow\am_pushsource_flags.htm
tech.root: DirectShow
ms.assetid: 878dc41b-8df3-4294-9e1f-7a3da1834ad1

ms.date: 12/05/2018
ms.keywords: AM_PUSHSOURCECAPS_INTERNAL_RM, AM_PUSHSOURCECAPS_NOT_LIVE, AM_PUSHSOURCECAPS_PRIVATE_CLOCK, AM_PUSHSOURCEREQS_USE_STREAM_CLOCK, AM_PUSHSOURCE_FLAGS, AM_PUSHSOURCE_FLAGSEnumeration, _AM_PUSHSOURCE_FLAGS, _AM_PUSHSOURCE_FLAGS enumeration [DirectShow], dshow.am_pushsource_flags, strmif/AM_PUSHSOURCECAPS_INTERNAL_RM, strmif/AM_PUSHSOURCECAPS_NOT_LIVE, strmif/AM_PUSHSOURCECAPS_PRIVATE_CLOCK, strmif/AM_PUSHSOURCEREQS_USE_STREAM_CLOCK, strmif/_AM_PUSHSOURCE_FLAGS
ms.topic: enum
f1_keywords: 
 - "strmif/_AM_PUSHSOURCE_FLAGS"
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
 - _AM_PUSHSOURCE_FLAGS
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# _AM_PUSHSOURCE_FLAGS enumeration


## -description



Indicates the behavior of a live source filter.




## -enum-fields




### -field AM_PUSHSOURCECAPS_INTERNAL_RM

The filter uses its own rate-matching mechanism; the renderer should therefore not attempt to match rates with this filter.
          


### -field AM_PUSHSOURCECAPS_NOT_LIVE

The filter is not live. Do not treat it as a live source, even though it exposes the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iampushsource">IAMPushSource</a> interface.
          


### -field AM_PUSHSOURCECAPS_PRIVATE_CLOCK

The filter time stamps the samples using a private clock. The clock is not available to the rest of the graph through <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ireferenceclock">IReferenceClock</a>.
          


### -field AM_PUSHSOURCEREQS_USE_STREAM_CLOCK

Reserved; do not use.
          


### -field AM_PUSHSOURCEREQS_USE_CLOCK_CHAIN




## -remarks



If no flags are set (the default case), the source filter is assumed to be live and not to perform any rate matching on its own.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>
 

 

