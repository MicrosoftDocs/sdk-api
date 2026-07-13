---
UID: NF:tapi.lineGetProviderListW
title: lineGetProviderListW function (tapi.h)
description: The lineGetProviderListW (Unicode) function (tapi.h) returns a list of service providers currently installed in the telephony system.
helpviewer_keywords: ["_tapi2_linegetproviderlist", "lineGetProviderList", "lineGetProviderList function [TAPI 2.2]", "lineGetProviderListW", "tapi/lineGetProviderList", "tapi/lineGetProviderListW", "tapi2.linegetproviderlist"]
old-location: tapi2\linegetproviderlist.htm
tech.root: tapi3
ms.assetid: 87d43409-e8c5-401a-87a2-02568ed0af4a
ms.date: 08/09/2022
ms.keywords: _tapi2_linegetproviderlist, lineGetProviderList, lineGetProviderList function [TAPI 2.2], lineGetProviderListA, lineGetProviderListW, tapi/lineGetProviderList, tapi/lineGetProviderListA, tapi/lineGetProviderListW, tapi2.linegetproviderlist
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineGetProviderListW (Unicode) and lineGetProviderListA (ANSI)
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
 - lineGetProviderListW
 - tapi/lineGetProviderListW
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
 - lineGetProviderList
 - lineGetProviderListA
 - lineGetProviderListW
---

# lineGetProviderListW function


## -description

The 
<b>lineGetProviderList</b> function returns a list of service providers currently installed in the telephony system.

## -parameters

### -param dwAPIVersion

Highest version of TAPI supported by the application (not necessarily the value negotiated by 
<a href="/windows/desktop/api/tapi/nf-tapi-linenegotiateapiversion">lineNegotiateAPIVersion</a> on some particular line device).

### -param lpProviderList

Pointer to a memory location where TAPI can return a 
<a href="/windows/desktop/api/tapi/ns-tapi-lineproviderlist">LINEPROVIDERLIST</a> structure. Prior to calling 
<b>lineGetProviderList</b>, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="/windows/desktop/Tapi/memory-allocation">memory allocation</a> topic. </div>
<div> </div>

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INCOMPATIBLEAPIVERSION, LINEERR_NOMEM, LINEERR_INIFILECORRUPT, LINEERR_OPERATIONFAILED, LINEERR_INVALPOINTER, LINEERR_STRUCTURETOOSMALL.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-lineproviderlist">LINEPROVIDERLIST</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linenegotiateapiversion">lineNegotiateAPIVersion</a>

## -remarks

> [!NOTE]
> The tapi.h header defines lineGetProviderList as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
