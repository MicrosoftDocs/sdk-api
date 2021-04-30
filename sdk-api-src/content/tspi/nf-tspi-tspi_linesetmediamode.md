---
UID: NF:tspi.TSPI_lineSetMediaMode
title: TSPI_lineSetMediaMode function (tspi.h)
description: The TSPI_lineSetMediaMode function changes the call's media as stored in the call's LINECALLINFO structure.
helpviewer_keywords: ["TSPI_lineSetMediaMode","TSPI_lineSetMediaMode function [TAPI 2.2]","_tspi_tspi_linesetmediamode","tspi.tspi_linesetmediamode","tspi/TSPI_lineSetMediaMode"]
old-location: tspi\tspi_linesetmediamode.htm
tech.root: tapi3
ms.assetid: 3a0a5daf-eb4a-4e60-b343-8a47d342a86a
ms.date: 12/05/2018
ms.keywords: TSPI_lineSetMediaMode, TSPI_lineSetMediaMode function [TAPI 2.2], _tspi_tspi_linesetmediamode, tspi.tspi_linesetmediamode, tspi/TSPI_lineSetMediaMode
req.header: tspi.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TSPI_lineSetMediaMode
 - tspi/TSPI_lineSetMediaMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_lineSetMediaMode
---

# TSPI_lineSetMediaMode function


## -description

The 
<b>TSPI_lineSetMediaMode</b> function changes the call's media as stored in the call's 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> structure.

## -parameters

### -param hdCall

The handle to the call undergoing a change in media type. The call state of <i>hdCall</i> can be any state.

### -param dwMediaMode

The new media type(s) for the call. As long as the LINEMEDIAMODE_UNKNOWN media type flag is set, multiple other media type flags can be set as well. This is used to identify a call's media type as not fully determined, but narrowed down to one of just a small set of specified media types. If the LINEMEDIAMODE_UNKNOWN flag is not set, only a single media type can be specified. This parameter uses one (or more) of the 
<a href="/windows/desktop/Tapi/linemediamode--constants">LINEMEDIAMODE_ constants</a>.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALMEDIAMODE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL.

## -remarks

Other than changing the call's media as stored in the call's 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> structure, this procedure is simply advisory in the sense that it indicates an expected media change that is about to occur, rather than forcing a specific change to the call. Typical usage is to set a call's media type to a specific known media type, or to exclude possible media types as long as the call's media type is not fully known (the UNKNOWN media type flag is set).

TAPI makes the following guarantees regarding the passed media type: (1) there is at least one bit set, (2) there are no reserved bits set, and (3) if more than one bit is set, "Unknown" is also set. The service provider must perform any further validity checks on the media types, such as checking whether any media types are indeed supported by the service provider.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>



<a href="/windows/desktop/Tapi/linemediamode--constants">LINEMEDIAMODE_ Constants</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetcallinfo">TSPI_lineGetCallInfo</a>