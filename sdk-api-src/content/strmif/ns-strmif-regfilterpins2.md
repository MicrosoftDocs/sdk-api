---
UID: NS:strmif.REGFILTERPINS2
title: REGFILTERPINS2 (strmif.h)
author: windows-sdk-content
description: The REGFILTERPINS2 structure contains information for registering a filter through the IFilterMapper2 interface.
old-location: dshow\regfilterpins2.htm
tech.root: DirectShow
ms.assetid: a78327f1-a0aa-4e25-b6f8-cf45b92191fa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: REGFILTERPINS2, REGFILTERPINS2 structure [DirectShow], REGFILTERPINS2Structure, dshow.regfilterpins2, strmif/REGFILTERPINS2
ms.topic: struct
f1_keywords: 
 - "strmif/REGFILTERPINS2"
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
 - REGFILTERPINS2
product: Windows
targetos: Windows
req.typenames: REGFILTERPINS2
req.redist: 
ms.custom: 19H1
---

# REGFILTERPINS2 structure


## -description



The <code>REGFILTERPINS2</code> structure contains information for registering a filter through the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifiltermapper2">IFilterMapper2</a> interface.




## -struct-fields




### -field dwFlags

Bitwise combination of zero or more <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd377518(v=vs.85)">REG_PINFLAG</a> flags.


### -field cInstances

Number of instances of this pin.


### -field nMediaTypes

Number of media types supported by this pin.


### -field lpMediaType

Pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-regpintypes">REGPINTYPES</a> structures, of size nMediaTypes.


### -field nMediums

Number of mediums. Can be zero.


### -field lpMedium

Pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-regpinmedium">REGPINMEDIUM</a> structures, of size nMediums.


### -field clsPinCategory

Optional pin category, from the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/pin-property-set">Pin Property Set</a>.


## -remarks



If you use this structure, set the <b>dwVersion</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-regfilter2">REGFILTER2</a> structure to 2.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>
 

 

