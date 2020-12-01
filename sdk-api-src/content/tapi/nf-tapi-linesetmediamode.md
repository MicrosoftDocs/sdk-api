---
UID: NF:tapi.lineSetMediaMode
title: lineSetMediaMode function (tapi.h)
description: The lineSetMediaMode function sets the media type(s) of the specified call in its LINECALLINFO structure. For more information, see ITLegacyCallMediaControl::SetMediaType.
helpviewer_keywords: ["_tapi2_linesetmediamode","lineSetMediaMode","lineSetMediaMode function [TAPI 2.2]","tapi/lineSetMediaMode","tapi2.linesetmediamode"]
old-location: tapi2\linesetmediamode.htm
tech.root: tapi3
ms.assetid: 4a0e3fd7-9483-4d21-9b6f-bb6c04aa8226
ms.date: 12/05/2018
ms.keywords: _tapi2_linesetmediamode, lineSetMediaMode, lineSetMediaMode function [TAPI 2.2], tapi/lineSetMediaMode, tapi2.linesetmediamode
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
 - lineSetMediaMode
 - tapi/lineSetMediaMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineSetMediaMode
---

# lineSetMediaMode function


## -description

The 
<b>lineSetMediaMode</b> function sets the media type(s) of the specified call in its 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> structure. For more information, see 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol-setmediatype">ITLegacyCallMediaControl::SetMediaType</a>.

## -parameters

### -param hCall

Handle to the call whose media type is to be changed. The application must be an owner of the call. The call state of <i>hCall</i> can be any state.

### -param dwMediaModes

New media type(s) for the call. This parameter uses the 
<a href="/windows/desktop/Tapi/linemediamode--constants">LINEMEDIAMODE_ Constants</a>. As long as the UNKNOWN media type flag is set, other media type flags may be set as well. This is used to identify a call's media type as not fully determined, but narrowed down to one of a small set of specified media types. If the UNKNOWN flag is not set, only a single media type can be specified.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALMEDIAMODE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_UNINITIALIZED, LINEERR_OPERATIONUNAVAIL.

## -remarks

The 
<b>lineSetMediaMode</b> function changes the call's media type in its 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> structure. Typical usage of this operation is either to set a call's media type to a specific known media type or to exclude possible media types as long as the call's media type is officially unknown (the UNKNOWN media type flag is set).

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>