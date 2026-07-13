---
UID: NF:tapi.lineAddProviderW
title: lineAddProviderW function (tapi.h)
description: The lineAddProviderW (Unicode) function (tapi.h) installs a new telephony service provider into the telephony system.
helpviewer_keywords: ["_tapi2_lineaddprovider", "lineAddProvider", "lineAddProvider function [TAPI 2.2]", "lineAddProviderW", "tapi/lineAddProvider", "tapi/lineAddProviderW", "tapi2.lineaddprovider"]
old-location: tapi2\lineaddprovider.htm
tech.root: tapi3
ms.assetid: d6c96dba-bbfb-4b4a-a4f5-a55fd4446f3b
ms.date: 08/08/2022
ms.keywords: _tapi2_lineaddprovider, lineAddProvider, lineAddProvider function [TAPI 2.2], lineAddProviderA, lineAddProviderW, tapi/lineAddProvider, tapi/lineAddProviderA, tapi/lineAddProviderW, tapi2.lineaddprovider
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineAddProviderW (Unicode) and lineAddProviderA (ANSI)
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
 - lineAddProviderW
 - tapi/lineAddProviderW
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
 - lineAddProvider
 - lineAddProviderA
 - lineAddProviderW
---

# lineAddProviderW function


## -description

The 
<b>lineAddProvider</b> function installs a new telephony service provider into the telephony system.

## -parameters

### -param lpszProviderFilename

Pointer to a <b></b>

<b>null</b>-terminated string containing the path of the service provider to be added.

### -param hwndOwner

Handle to a window in which any dialog boxes that need to be displayed as part of the installation process (for example, by the service provider's 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerinstall">TSPI_providerInstall</a> function) would be attached. Can be <b>NULL</b> to indicate that any window created during the function should have no owner window.

### -param lpdwPermanentProviderID

Pointer to a variable that receives the permanent provider identifier of the newly installed service provider.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INIFILECORRUPT, LINEERR_INVALPARAM, LINEERR_INVALPOINTER, LINEERR_NOMEM, LINEERR_NOMULTIPLEINSTANCE, LINEERR_OPERATIONFAILED.

## -remarks

During this function call, TAPI checks to ensure that it can access the service provider by calling its 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerinstall">TSPI_providerInstall</a> function; if this is unsuccessful (if the DLL or function cannot be found, or if 
<b>TSPI_providerInstall</b> returns an error), the function fails and the provider is not added to the telephony system. If this succeeds, and the  Telephony system is active (one or more applications have called 
<a href="/windows/desktop/api/tapi/nf-tapi-lineinitialize">lineInitialize</a> or 
<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>), TAPI does not attempt to launch the newly-added service provider. Instead, in order to activate the new service provider, TAPI issues a message to restart Windows. When the activation succeeds, applications are informed of any new devices created by way of 
<a href="/windows/desktop/Tapi/line-create">LINE_CREATE</a> or 
<a href="/windows/desktop/Tapi/phone-create">PHONE_CREATE</a> messages, or by a 
<a href="/windows/desktop/Tapi/line-linedevstate">LINE_LINEDEVSTATE</a> message requesting reinitialization (if the application does not support the CREATE messages).

This function copies no files—not the service provider DLL itself nor any supporting files; the application managing the addition of the provider must ensure that the provider is installed in a directory where it can be found by TAPI (for example, \WINDOWS, \WINDOWS\SYSTEM, or elsewhere on the path).





> [!NOTE]
> The tapi.h header defines lineAddProvider as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Tapi/line-create">LINE_CREATE</a>



<a href="/windows/desktop/Tapi/line-linedevstate">LINE_LINEDEVSTATE</a>



<a href="/windows/desktop/Tapi/phone-create">PHONE_CREATE</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineinitialize">lineInitialize</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>
