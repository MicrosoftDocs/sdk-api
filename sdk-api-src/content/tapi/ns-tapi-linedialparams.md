---
UID: NS:tapi.linedialparams_tag
title: LINEDIALPARAMS (tapi.h)
description: The LINEDIALPARAMS structure specifies a collection of dialing-related fields. Call the lineSetCallParams function or the TSPI_lineSetCallParams function to set parameters for a call using the LINEDIALPARAMS structure.
helpviewer_keywords: ["*LPLINEDIALPARAMS","LINEDIALPARAMS","LINEDIALPARAMS structure [TAPI 2.2]","LPLINEDIALPARAMS","LPLINEDIALPARAMS structure pointer [TAPI 2.2]","_tapi2_linedialparams_str","tapi/LINEDIALPARAMS","tapi/LPLINEDIALPARAMS","tapi2.linedialparams_str"]
old-location: tapi2\linedialparams_str.htm
tech.root: tapi3
ms.assetid: efb65462-abe5-46db-9299-97871e0d011e
ms.date: 12/05/2018
ms.keywords: '*LPLINEDIALPARAMS, LINEDIALPARAMS, LINEDIALPARAMS structure [TAPI 2.2], LPLINEDIALPARAMS, LPLINEDIALPARAMS structure pointer [TAPI 2.2], _tapi2_linedialparams_str, tapi/LINEDIALPARAMS, tapi/LPLINEDIALPARAMS, tapi2.linedialparams_str'
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
req.typenames: LINEDIALPARAMS, *LPLINEDIALPARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - linedialparams_tag
 - tapi/linedialparams_tag
 - LPLINEDIALPARAMS
 - tapi/LPLINEDIALPARAMS
 - LINEDIALPARAMS
 - tapi/LINEDIALPARAMS
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
 - LINEDIALPARAMS
---

# LINEDIALPARAMS structure


## -description

The 
<b>LINEDIALPARAMS</b> structure specifies a collection of dialing-related fields. Call the 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetcallparams">lineSetCallParams</a> function or the 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetcallparams">TSPI_lineSetCallParams</a> function to set parameters for a call using the 
<b>LINEDIALPARAMS</b> structure.

## -struct-fields

### -field dwDialPause

Duration of a comma in the dialable address, in milliseconds.

### -field dwDialSpeed

Interdigit time period between successive digits, in milliseconds.

### -field dwDigitDuration

Duration of a digit, in milliseconds.

### -field dwWaitForDialtone

Maximum amount of time to wait for a dial tone when a 'W' is used in the dialable address, in milliseconds.

## -remarks

This structure may not be extended.

If zero is specified for a member, the default value is used. If a nonzero value is specified for a member that is outside the range specified by the <b>MinDialParams</b> and <b>MaxDialParams</b> members in the 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a> structure, the nearest value within the valid range is used instead.

The 
<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a> function allows an application to adjust the dialing parameters to be used for the call. The 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetcallparams">lineSetCallParams</a> function can be used to adjust the dialing parameters of an existing call. The 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> structure lists the call's current dialing parameters.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetcallparams">TSPI_lineSetCallParams</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetcallparams">lineSetCallParams</a>