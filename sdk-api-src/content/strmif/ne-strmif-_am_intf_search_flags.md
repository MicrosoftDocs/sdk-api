---
UID: NE:strmif._AM_INTF_SEARCH_FLAGS
title: "_AM_INTF_SEARCH_FLAGS"
author: windows-sdk-content
description: Specifies the types of object to search, when attempting to find an interface on the filter graph.
old-location: dshow\am_intf_search_flags.htm
tech.root: DirectShow
ms.assetid: 090c19c8-eb38-4185-9f6b-169495f9ab27
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: AM_INTF_SEARCH_FILTER, AM_INTF_SEARCH_FLAGS, AM_INTF_SEARCH_FLAGSEnumeration, AM_INTF_SEARCH_INPUT_PIN, AM_INTF_SEARCH_OUTPUT_PIN, _AM_INTF_SEARCH_FLAGS, _AM_INTF_SEARCH_FLAGS enumeration [DirectShow], dshow.am_intf_search_flags, strmif/AM_INTF_SEARCH_FILTER, strmif/AM_INTF_SEARCH_INPUT_PIN, strmif/AM_INTF_SEARCH_OUTPUT_PIN, strmif/_AM_INTF_SEARCH_FLAGS
ms.prod: windows
ms.technology: windows-sdk
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
 - _AM_INTF_SEARCH_FLAGS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# _AM_INTF_SEARCH_FLAGS enumeration


## -description



Specifies the types of object to search, when attempting to find an interface on the filter graph.




## -enum-fields




### -field AM_INTF_SEARCH_INPUT_PIN

Search input pins.


### -field AM_INTF_SEARCH_OUTPUT_PIN

Search output pins.


### -field AM_INTF_SEARCH_FILTER

Search filters.


## -remarks



If no flags are set (the default case), it is equivalent to the bitwise <b>OR</b> of all the flags. All filters and pins are searched.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/23106ef0-e5ce-47a6-97b0-518bb78ec67c">IAMGraphStreams::FindUpstreamInterface</a>
 

 

