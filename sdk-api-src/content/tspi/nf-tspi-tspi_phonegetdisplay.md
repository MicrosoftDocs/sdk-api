---
UID: NF:tspi.TSPI_phoneGetDisplay
title: TSPI_phoneGetDisplay function (tspi.h)
description: The TSPI_phoneGetDisplay function returns the current contents of the specified phone display.
helpviewer_keywords: ["TSPI_phoneGetDisplay","TSPI_phoneGetDisplay function [TAPI 2.2]","_tspi_tspi_phonegetdisplay","tspi.tspi_phonegetdisplay","tspi/TSPI_phoneGetDisplay"]
old-location: tspi\tspi_phonegetdisplay.htm
tech.root: tapi3
ms.assetid: dff5fdc5-a627-4282-85d3-2a7ceaf063ed
ms.date: 12/05/2018
ms.keywords: TSPI_phoneGetDisplay, TSPI_phoneGetDisplay function [TAPI 2.2], _tspi_tspi_phonegetdisplay, tspi.tspi_phonegetdisplay, tspi/TSPI_phoneGetDisplay
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
 - TSPI_phoneGetDisplay
 - tspi/TSPI_phoneGetDisplay
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
 - TSPI_phoneGetDisplay
---

# TSPI_phoneGetDisplay function


## -description

The 
<b>TSPI_phoneGetDisplay</b> function returns the current contents of the specified phone display.

## -parameters

### -param hdPhone

The handle to the phone to be queried.

### -param lpDisplay

A pointer to the memory location where the display content is to be stored by the provider, of type 
<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a>. Prior to calling 
<b>TSPI_phoneGetDisplay</b>, the application sets the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_NOMEM, PHONEERR_OPERATIONUNAVAIL.

## -remarks

The <i>lpDisplay</i> memory area should be at least <b>dwDisplayNumRows</b> * <b>dwDisplayNumColumns</b> elements in size to receive all of the display information. The <b>dwDisplayNumRows</b> and <b>dwDisplayNumColumns</b> members are available in the 
<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a> structure returned by 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetdevcaps">TSPI_phoneGetDevCaps</a>.

The service provider fills in all the members of the 
<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a> data structure, except for <b>dwTotalSize</b>, which is filled in by TAPI. The service provider must not overwrite the <b>dwTotalSize</b> member.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetdevcaps">TSPI_phoneGetDevCaps</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonesetdisplay">TSPI_phoneSetDisplay</a>



<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a>