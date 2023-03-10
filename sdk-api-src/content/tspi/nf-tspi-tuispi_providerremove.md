---
UID: NF:tspi.TUISPI_providerRemove
title: TUISPI_providerRemove function (tspi.h)
description: The TUISPI_providerRemove function asks the user to confirm elimination of the service provider. This function makes the TSPI_providerRemove function obsolete in version 2.0 and later (supported in version 1.4 and earlier).
helpviewer_keywords: ["TUISPI_providerRemove","TUISPI_providerRemove function [TAPI 2.2]","_tspi_tuispi_providerremove","tspi.tuispi_providerremove","tspi/TUISPI_providerRemove"]
old-location: tspi\tuispi_providerremove.htm
tech.root: tapi3
ms.assetid: 217d1f40-7f3f-49a0-b29e-e2da85ba47f1
ms.date: 12/05/2018
ms.keywords: TUISPI_providerRemove, TUISPI_providerRemove function [TAPI 2.2], _tspi_tuispi_providerremove, tspi.tuispi_providerremove, tspi/TUISPI_providerRemove
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
 - TUISPI_providerRemove
 - tspi/TUISPI_providerRemove
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
 - TUISPI_providerRemove
---

# TUISPI_providerRemove function


## -description

The 
<b>TUISPI_providerRemove</b> function asks the user to confirm elimination of the service provider. This function makes the 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerremove">TSPI_providerRemove</a> function obsolete in version 2.0 and later (supported in version 1.4 and earlier).

It is the responsibility of the service provider to remove any registry entries that the service provider added at <b>addProvider</b> time, as well as any other modules and files that are no longer needed.

Implementation is optional.

## -parameters

### -param lpfnUIDLLCallback

Pointer to a function the UI DLL can call to communicate with the service provider DLL to obtain information needed to display the dialog box.

### -param hwndOwner

The handle of the parent window in which the function can create any dialog box windows required during the removal.

### -param dwPermanentProviderID

The service provider's permanent provider identifier.

## -returns

Returns zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_OPERATIONFAILED, LINEERR_INIFILECORRUPT, LINEERR_NOMEM, LINEERR_INVALPARAM.

## -remarks

This function must guarantee that any service provider's privately-defined information is removed from the registry if it returns success.

This procedure must leave the system in a consistent state. It should run to completion, not allowing the user to abort the removal when it is partly completed. If removal fails, it is the provider's responsibility to "back out" what was done and return an error. This may imply pre-scanning to verify that a complete removal is possible, before the removal begins.

This function can be called while the service provider is in use (that is, between 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerinit">TSPI_providerInit</a> and 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providershutdown">TSPI_providerShutdown</a>). If this happens, the service provider should do an appropriate combination of displaying a user dialog box to announce any conflict and confirm removal, restricting removal options to those that can be performed transparently, or issuing 
<a href="/previous-versions/windows/desktop/legacy/ms725220(v=vs.85)">LINE_CLOSE</a> and 
<a href="/previous-versions/windows/desktop/legacy/ms725255(v=vs.85)">PHONE_CLOSE</a> messages to inform TAPI and applications that the affected devices have been forcibly closed for removal. In any case, any changes that affect the behavior visible through TSPI should take effect only when the service provider is shut down at the next 
<b>TSPI_providerShutdown</b>.

<div class="alert"><b>Note</b>  This function should not return LINEERR_INUSE or other errors that might occur because the provider is in use by an application; instead, the provider should confer with the user directly about this problem, and then return LINEERR_OPERATIONFAILED if the user decides to abort the operation.</div>
<div> </div>
This procedure is called only once, at the time of removal of the service provider, until there is a call to 
<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providerinstall">TUISPI_providerInstall</a>.

The corresponding function at the TAPI level is 
<a href="/windows/desktop/api/tapi/nf-tapi-lineremoveprovider">lineRemoveProvider</a>. At that level, applications expect to have service providers already installed; otherwise their lines and phones do not appear within the available sequence of device identifiers. The 
<a href="/previous-versions/windows/desktop/legacy/ms725223(v=vs.85)">LINE_CREATE</a> message informs applications that are running about dynamic reconfiguration.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms725220(v=vs.85)">LINE_CLOSE</a>



<a href="/previous-versions/windows/desktop/legacy/ms725255(v=vs.85)">PHONE_CLOSE</a>



<a href="/previous-versions/windows/desktop/legacy/ms725262(v=vs.85)">PHONE_STATE</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerinit">TSPI_providerInit</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providershutdown">TSPI_providerShutdown</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providerinstall">TUISPI_providerInstall</a>