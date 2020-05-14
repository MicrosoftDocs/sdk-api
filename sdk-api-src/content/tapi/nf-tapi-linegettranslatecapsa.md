---
UID: NF:tapi.lineGetTranslateCapsA
title: lineGetTranslateCapsA function (tapi.h)
description: The lineGetTranslateCaps function returns address translation capabilities.helpviewer_keywords: ["_tapi2_linegettranslatecaps","lineGetTranslateCaps","lineGetTranslateCaps function [TAPI 2.2]","lineGetTranslateCapsA","lineGetTranslateCapsW","tapi/lineGetTranslateCaps","tapi/lineGetTranslateCapsA","tapi/lineGetTranslateCapsW","tapi2.linegettranslatecaps"]
old-location: tapi2\linegettranslatecaps.htm
tech.root: Tapi
ms.assetid: 77437b06-fb02-44b5-8642-b3de700853ef
ms.date: 12/05/2018
ms.keywords: _tapi2_linegettranslatecaps, lineGetTranslateCaps, lineGetTranslateCaps function [TAPI 2.2], lineGetTranslateCapsA, lineGetTranslateCapsW, tapi/lineGetTranslateCaps, tapi/lineGetTranslateCapsA, tapi/lineGetTranslateCapsW, tapi2.linegettranslatecaps
f1_keywords:
- tapi/lineGetTranslateCaps
dev_langs:
- c++
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineGetTranslateCapsW (Unicode) and lineGetTranslateCapsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Tapi32.dll
api_name:
- lineGetTranslateCaps
- lineGetTranslateCapsA
- lineGetTranslateCapsW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# lineGetTranslateCapsA function


## -description


The 
<b>lineGetTranslateCaps</b> function returns address translation capabilities.


## -parameters




### -param hLineApp

Handle returned by the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a> function. If an application has not yet called the 
<b>lineInitializeEx</b> function, this parameter can be zero.

<div class="alert"><b>Note</b>   TAPI 1.4 applications must set this parameter to a valid hLineApp handle, as returned by the <a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-lineinitialize">lineInitialize</a> function.

</div>
<div> </div>

### -param dwAPIVersion

Highest version of TAPI supported by the application (not necessarily the value negotiated by 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linenegotiateapiversion">lineNegotiateAPIVersion</a> on some particular line device).


### -param lpTranslateCaps

Pointer to a location to which a 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-linetranslatecaps">LINETRANSLATECAPS</a> structure is loaded. Prior to calling 
<b>lineGetTranslateCaps</b>, the application must  set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/memory-allocation">memory allocation</a> topic.</div>
<div> </div>

## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INCOMPATIBLEAPIVERSION, LINEERR_NOMEM, LINEERR_INIFILECORRUPT, LINEERR_OPERATIONFAILED, LINEERR_INVALAPPHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_STRUCTURETOOSMALL, LINEERR_NODRIVER.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-linetranslatecaps">LINETRANSLATECAPS</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linenegotiateapiversion">lineNegotiateAPIVersion</a>
 

 

