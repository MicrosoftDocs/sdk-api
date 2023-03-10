---
UID: NS:tapi.lineforwardlist_tag
title: LINEFORWARDLIST (tapi.h)
description: The LINEFORWARDLIST structure describes a list of forwarding instructions. This structure can contain an array of LINEFORWARD structures. The lineForward and TSPI_lineForward functions use the LINEFORWARDLIST structure.
helpviewer_keywords: ["*LPLINEFORWARDLIST","LINEFORWARDLIST","LINEFORWARDLIST structure [TAPI 2.2]","LPLINEFORWARDLIST","LPLINEFORWARDLIST structure pointer [TAPI 2.2]","_tapi2_lineforwardlist_str","tapi/LINEFORWARDLIST","tapi/LPLINEFORWARDLIST","tapi2.lineforwardlist_str"]
old-location: tapi2\lineforwardlist_str.htm
tech.root: tapi3
ms.assetid: 3dec9ab6-43d8-4dda-b0b1-a25407e4d77a
ms.date: 12/05/2018
ms.keywords: '*LPLINEFORWARDLIST, LINEFORWARDLIST, LINEFORWARDLIST structure [TAPI 2.2], LPLINEFORWARDLIST, LPLINEFORWARDLIST structure pointer [TAPI 2.2], _tapi2_lineforwardlist_str, tapi/LINEFORWARDLIST, tapi/LPLINEFORWARDLIST, tapi2.lineforwardlist_str'
req.header: tapi.h
req.include-header: 
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
req.typenames: LINEFORWARDLIST, *LPLINEFORWARDLIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineforwardlist_tag
 - tapi/lineforwardlist_tag
 - LPLINEFORWARDLIST
 - tapi/LPLINEFORWARDLIST
 - LINEFORWARDLIST
 - tapi/LINEFORWARDLIST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEFORWARDLIST
---

# LINEFORWARDLIST structure


## -description

The 
<b>LINEFORWARDLIST</b> structure describes a list of forwarding instructions. This structure can contain an array of 
<a href="/windows/desktop/api/tapi/ns-tapi-lineforward">LINEFORWARD</a> structures. The 
<a href="/windows/desktop/api/tapi/nf-tapi-lineforward">lineForward</a> and 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineforward">TSPI_lineForward</a> functions use the 
<b>LINEFORWARDLIST</b> structure.

## -struct-fields

### -field dwTotalSize

Total size of the data structure, in bytes.

### -field dwNumEntries

Number of entries in the array specified as <b>ForwardList[]</b>.

### -field ForwardList

Array of forwarding instruction. The array's entries are of type 
<a href="/windows/desktop/api/tapi/ns-tapi-lineforward">LINEFORWARD</a>.

## -remarks

This structure may not be extended.

The 
<b>LINEFORWARDLIST</b> structure defines the forwarding parameters requested for forwarding calls on an address or on all addresses on a line.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-lineforward">LINEFORWARD</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineforward">TSPI_lineForward</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineforward">lineForward</a>