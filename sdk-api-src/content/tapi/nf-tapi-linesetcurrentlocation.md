---
UID: NF:tapi.lineSetCurrentLocation
title: lineSetCurrentLocation function (tapi.h)
description: The lineSetCurrentLocation function sets the location used as the context for address translation.
helpviewer_keywords: ["_tapi2_linesetcurrentlocation","lineSetCurrentLocation","lineSetCurrentLocation function [TAPI 2.2]","tapi/lineSetCurrentLocation","tapi2.linesetcurrentlocation"]
old-location: tapi2\linesetcurrentlocation.htm
tech.root: tapi3
ms.assetid: ad31bc8b-399d-4c2e-b79c-fc935d5adf1a
ms.date: 12/05/2018
ms.keywords: _tapi2_linesetcurrentlocation, lineSetCurrentLocation, lineSetCurrentLocation function [TAPI 2.2], tapi/lineSetCurrentLocation, tapi2.linesetcurrentlocation
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
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineSetCurrentLocation
 - tapi/lineSetCurrentLocation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ras-tapi32-l1-1-1.dll
 - Tapi32.dll
api_name:
 - lineSetCurrentLocation
---

# lineSetCurrentLocation function


## -description

The 
<b>lineSetCurrentLocation</b> function sets the location used as the context for address translation.

## -parameters

### -param hLineApp

Application handle returned by 
<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>. If an application has not yet called the 
<b>lineInitializeEx</b> function, it can set the <i>hLineApp</i> parameter to zero.

### -param dwLocation

New value for the CurrentLocation entry in the [Locations] section in the registry. It must contain a valid permanent identifier of a Location entry in the [Locations] section, as obtained from 
<a href="/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">lineGetTranslateCaps</a>. If it is valid, the CurrentLocation entry is updated.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INIFILECORRUPT, LINEERR_NOMEM, LINEERR_INVALAPPHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALLOCATION, LINEERR_RESOURCEUNAVAIL, LINEERR_NODRIVER, LINEERR_UNINITIALIZED.

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">lineGetTranslateCaps</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>