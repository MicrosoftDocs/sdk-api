---
UID: NE:strmif._AM_INTF_SEARCH_FLAGS
title: "_AM_INTF_SEARCH_FLAGS (strmif.h)"
description: Specifies the types of object to search, when attempting to find an interface on the filter graph.
helpviewer_keywords: ["AM_INTF_SEARCH_FILTER","AM_INTF_SEARCH_FLAGS","AM_INTF_SEARCH_FLAGSEnumeration","AM_INTF_SEARCH_INPUT_PIN","AM_INTF_SEARCH_OUTPUT_PIN","_AM_INTF_SEARCH_FLAGS","_AM_INTF_SEARCH_FLAGS enumeration [DirectShow]","dshow.am_intf_search_flags","strmif/AM_INTF_SEARCH_FILTER","strmif/AM_INTF_SEARCH_INPUT_PIN","strmif/AM_INTF_SEARCH_OUTPUT_PIN","strmif/_AM_INTF_SEARCH_FLAGS"]
old-location: dshow\am_intf_search_flags.htm
tech.root: dshow
ms.assetid: 090c19c8-eb38-4185-9f6b-169495f9ab27
ms.date: 12/05/2018
ms.keywords: AM_INTF_SEARCH_FILTER, AM_INTF_SEARCH_FLAGS, AM_INTF_SEARCH_FLAGSEnumeration, AM_INTF_SEARCH_INPUT_PIN, AM_INTF_SEARCH_OUTPUT_PIN, _AM_INTF_SEARCH_FLAGS, _AM_INTF_SEARCH_FLAGS enumeration [DirectShow], dshow.am_intf_search_flags, strmif/AM_INTF_SEARCH_FILTER, strmif/AM_INTF_SEARCH_INPUT_PIN, strmif/AM_INTF_SEARCH_OUTPUT_PIN, strmif/_AM_INTF_SEARCH_FLAGS
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
 - _AM_INTF_SEARCH_FLAGS
 - strmif/_AM_INTF_SEARCH_FLAGS
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
 - _AM_INTF_SEARCH_FLAGS
---

# _AM_INTF_SEARCH_FLAGS enumeration


## -description

Specifies the types of object to search, when attempting to find an interface on the filter graph.

## -enum-fields

### -field AM_INTF_SEARCH_INPUT_PIN:0x1

Search input pins.

### -field AM_INTF_SEARCH_OUTPUT_PIN:0x2

Search output pins.

### -field AM_INTF_SEARCH_FILTER:0x4

Search filters.

## -remarks

If no flags are set (the default case), it is equivalent to the bitwise <b>OR</b> of all the flags. All filters and pins are searched.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamgraphstreams-findupstreaminterface">IAMGraphStreams::FindUpstreamInterface</a>
