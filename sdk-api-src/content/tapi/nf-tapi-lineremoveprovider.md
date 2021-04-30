---
UID: NF:tapi.lineRemoveProvider
title: lineRemoveProvider function (tapi.h)
description: The lineRemoveProvider function removes an existing telephony service provider from the telephony system.
helpviewer_keywords: ["_tapi2_lineremoveprovider","lineRemoveProvider","lineRemoveProvider function [TAPI 2.2]","tapi/lineRemoveProvider","tapi2.lineremoveprovider"]
old-location: tapi2\lineremoveprovider.htm
tech.root: tapi3
ms.assetid: 8398a869-bc64-490a-bdb2-496582a88d84
ms.date: 12/05/2018
ms.keywords: _tapi2_lineremoveprovider, lineRemoveProvider, lineRemoveProvider function [TAPI 2.2], tapi/lineRemoveProvider, tapi2.lineremoveprovider
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
 - lineRemoveProvider
 - tapi/lineRemoveProvider
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
 - lineRemoveProvider
---

# lineRemoveProvider function


## -description

The 
<b>lineRemoveProvider</b> function removes an existing telephony service provider from the telephony system.

## -parameters

### -param dwPermanentProviderID

Permanent provider identifier of the service provider to be removed.

### -param hwndOwner

Handle to a window to which any dialog boxes that need to be displayed as part of the removal process (for example, a confirmation dialog box by the service provider's 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerremove">TSPI_providerRemove</a> function) would be attached. Can be a <b>NULL</b> value to indicate that any window created during the function should have no owner window.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INIFILECORRUPT, LINEERR_NOMEM, LINEERR_INVALPARAM, LINEERR_OPERATIONFAILED.

## -remarks

If the call to 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerremove">TSPI_providerRemove</a> succeeds, and the telephony system is active at the time, TAPI calls 
<a href="/windows/desktop/api/tapi/nf-tapi-lineshutdown">lineShutdown</a> and/or 
<a href="/windows/desktop/api/tapi/nf-tapi-phoneshutdown">phoneShutdown</a> on the service provider (depending on which device types are active). Any line or phone handles still held by applications on associated devices are forcibly closed with 
<a href="/windows/desktop/Tapi/line-close">LINE_CLOSE</a> or 
<a href="/windows/desktop/Tapi/phone-close">PHONE_CLOSE</a> messages (it is preferable for service providers to issue these messages as part of 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerremove">TSPI_providerRemove</a>, after verification with the user). The devices previously under the control of that provider are then marked as "unavailable", so that any future attempts by applications to reference them by device identifier result in LINEERR_NODRIVER.

## -see-also

<a href="/windows/desktop/Tapi/line-close">LINE_CLOSE</a>



<a href="/windows/desktop/Tapi/phone-close">PHONE_CLOSE</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>