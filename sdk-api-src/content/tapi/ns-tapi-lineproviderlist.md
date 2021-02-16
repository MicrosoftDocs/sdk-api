---
UID: NS:tapi.lineproviderlist_tag
title: LINEPROVIDERLIST (tapi.h)
description: The LINEPROVIDERLIST structure describes a list of service providers. A structure of this type is returned by the lineGetProviderList function. The LINEPROVIDERLIST structure can contain an array of LINEPROVIDERENTRY structures.
helpviewer_keywords: ["*LPLINEPROVIDERLIST","LINEPROVIDERLIST","LINEPROVIDERLIST structure [TAPI 2.2]","LPLINEPROVIDERLIST","LPLINEPROVIDERLIST structure pointer [TAPI 2.2]","_tapi2_lineproviderlist_str","tapi/LINEPROVIDERLIST","tapi/LPLINEPROVIDERLIST","tapi2.lineproviderlist_str"]
old-location: tapi2\lineproviderlist_str.htm
tech.root: tapi3
ms.assetid: 75790ffd-bb1b-4efc-a905-5727d31f8aec
ms.date: 12/05/2018
ms.keywords: '*LPLINEPROVIDERLIST, LINEPROVIDERLIST, LINEPROVIDERLIST structure [TAPI 2.2], LPLINEPROVIDERLIST, LPLINEPROVIDERLIST structure pointer [TAPI 2.2], _tapi2_lineproviderlist_str, tapi/LINEPROVIDERLIST, tapi/LPLINEPROVIDERLIST, tapi2.lineproviderlist_str'
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
req.typenames: LINEPROVIDERLIST, *LPLINEPROVIDERLIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineproviderlist_tag
 - tapi/lineproviderlist_tag
 - LPLINEPROVIDERLIST
 - tapi/LPLINEPROVIDERLIST
 - LINEPROVIDERLIST
 - tapi/LINEPROVIDERLIST
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
 - LINEPROVIDERLIST
---

# LINEPROVIDERLIST structure


## -description

The 
<b>LINEPROVIDERLIST</b> structure describes a list of service providers. A structure of this type is returned by the 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetproviderlist">lineGetProviderList</a> function. The 
<b>LINEPROVIDERLIST</b> structure can contain an array of 
<a href="/windows/desktop/api/tapi/ns-tapi-lineproviderentry">LINEPROVIDERENTRY</a> structures.

## -struct-fields

### -field dwTotalSize

Total size allocated to this data structure, in bytes.

### -field dwNeededSize

Size for this data structure that is needed to hold all the returned information, in bytes.

### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.

### -field dwNumProviders

Number of 
<a href="/windows/desktop/api/tapi/ns-tapi-lineproviderentry">LINEPROVIDERENTRY</a> structures present in the array denominated by <b>dwProviderListSize</b> and <b>dwProviderListOffset</b>.

### -field dwProviderListSize

Size of the provider list array, in bytes.

### -field dwProviderListOffset

Offset from the beginning of this structure to an array of 
<a href="/windows/desktop/api/tapi/ns-tapi-lineproviderentry">LINEPROVIDERENTRY</a> elements, which provide the information on each service provider. The size of the array is specified by <b>dwProviderListSize</b>.

## -remarks

This structure may not be extended.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-lineproviderentry">LINEPROVIDERENTRY</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetproviderlist">lineGetProviderList</a>