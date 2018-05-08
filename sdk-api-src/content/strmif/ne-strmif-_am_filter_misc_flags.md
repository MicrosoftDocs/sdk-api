---
UID: NE:strmif._AM_FILTER_MISC_FLAGS
title: "_AM_FILTER_MISC_FLAGS"
author: windows-driver-content
description: The _AM_FILTER_MISC_FLAGS enumeration contains flags that indicate whether a filter is a source filter or a renderer filter.
old-location: dshow\_am_filter_misc_flags.htm
old-project: DirectShow
ms.assetid: 7acc160c-0da8-4b85-b88c-82b59ec38106
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: AM_FILTER_MISC_FLAGSEnumeration, AM_FILTER_MISC_FLAGS_IS_RENDERER, AM_FILTER_MISC_FLAGS_IS_SOURCE, _AM_FILTER_MISC_FLAGS, _AM_FILTER_MISC_FLAGS enumeration [DirectShow], dshow._am_filter_misc_flags, strmif/AM_FILTER_MISC_FLAGS_IS_RENDERER, strmif/AM_FILTER_MISC_FLAGS_IS_SOURCE, strmif/_AM_FILTER_MISC_FLAGS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Strmif.h
api_name:
-	_AM_FILTER_MISC_FLAGS
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1
---

# _AM_FILTER_MISC_FLAGS enumeration


## -description



The <b>_AM_FILTER_MISC_FLAGS</b> enumeration contains flags that indicate whether a filter is a source filter or a renderer filter.




## -enum-fields




### -field AM_FILTER_MISC_FLAGS_IS_RENDERER

The filter is a renderer and sends an <a href="https://msdn.microsoft.com/46037d53-085d-4fd0-91a0-408702cbfce5">EC_COMPLETE</a> event at the end of the stream.


### -field AM_FILTER_MISC_FLAGS_IS_SOURCE

The filter is a source filter.


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/03728d28-a3e5-4ac5-b637-1daa173e5e88">IAMFilterMiscFlags::GetMiscFlags</a>
 

 

