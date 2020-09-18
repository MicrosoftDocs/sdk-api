---
UID: NF:tapi.lineConfigProvider
title: lineConfigProvider function (tapi.h)
description: The lineConfigProvider function causes a service provider to display its configuration dialog box.
helpviewer_keywords: ["_tapi2_lineconfigprovider","lineConfigProvider","lineConfigProvider function [TAPI 2.2]","tapi/lineConfigProvider","tapi2.lineconfigprovider"]
old-location: tapi2\lineconfigprovider.htm
tech.root: tapi3
ms.assetid: 3149b353-6380-4fa9-a6ef-cf4566aaff58
ms.date: 12/05/2018
ms.keywords: _tapi2_lineconfigprovider, lineConfigProvider, lineConfigProvider function [TAPI 2.2], tapi/lineConfigProvider, tapi2.lineconfigprovider
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
 - lineConfigProvider
 - tapi/lineConfigProvider
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
 - lineConfigProvider
---

# lineConfigProvider function


## -description

The 
<b>lineConfigProvider</b> function causes a service provider to display its configuration dialog box.

## -parameters

### -param hwndOwner

Handle to a window to which the configuration dialog box (displayed by 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerconfig">TSPI_providerConfig</a>) is attached. Can be <b>NULL</b> to indicate that any window created during the function should have no owner window.

### -param dwPermanentProviderID

Permanent provider identifier of the service provider to be configured.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INIFILECORRUPT, LINEERR_NOMEM, LINEERR_INVALPARAM, LINEERR_OPERATIONFAILED.

## -remarks

This is basically a straight pass-through to 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerconfig">TSPI_providerConfig</a>.

## -see-also

<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>