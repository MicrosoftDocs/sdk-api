---
UID: NF:tspi.TUISPI_providerInstall
title: TUISPI_providerInstall function (tspi.h)
description: Implementation of the TUISPI_providerInstall function is the service provider's opportunity to install any additional &quot;pieces&quot; of the provider into the right directories and set up registry entries the provider needs.
helpviewer_keywords: ["TUISPI_providerInstall","TUISPI_providerInstall function [TAPI 2.2]","_tspi_tuispi_providerinstall","tspi.tuispi_providerinstall","tspi/TUISPI_providerInstall"]
old-location: tspi\tuispi_providerinstall.htm
tech.root: tapi3
ms.assetid: 4b133336-7cd1-4af4-bc8d-4defce97559d
ms.date: 12/05/2018
ms.keywords: TUISPI_providerInstall, TUISPI_providerInstall function [TAPI 2.2], _tspi_tuispi_providerinstall, tspi.tuispi_providerinstall, tspi/TUISPI_providerInstall
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
 - TUISPI_providerInstall
 - tspi/TUISPI_providerInstall
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
 - TUISPI_providerInstall
---

# TUISPI_providerInstall function


## -description

Implementation of the 
<b>TUISPI_providerInstall</b> function is the service provider's opportunity to install any additional "pieces" of the provider into the right directories (or at least verifying that they're there) and set up registry entries the provider needs. This function makes the 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerinstall">TSPI_providerInstall</a> function obsolete in version 2.0 and later (supported in version 1.4 and earlier).

If the service provider requires any privately-defined entries in the registry for proper operation, they must be installed at this time.

Implementation is optional.

## -parameters

### -param lpfnUIDLLCallback

Pointer to a function the UI DLL can call to communicate with the service provider DLL to obtain information needed to display the dialog box.

### -param hwndOwner

The handle of the parent window in which the function can create any dialog box windows that are required during installation.

### -param dwPermanentProviderID

The service provider's permanent provider identifier.

## -returns

Returns zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_OPERATIONFAILED, LINEERR_INIFILECORRUPT, LINEERR_NOMEM. LINEERR_INVALPARAM.

## -remarks

This function must leave the system in a consistent state. It should run to completion, not allowing the user to abort the installation when it is partly completed. If installation fails, it is the provider's responsibility to "back out" what was done and return an error. This may imply pre-scanning to verify that a complete installation is possible, before the installation begins.

This function can be invoked more than once during installation of the service provider, until there is a call to 
<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providerremove">TUISPI_providerRemove</a>. If the service provider does not require or support multiple instances of the provider, however, it returns the 
<a href="/windows/desktop/Tapi/lineerr--constants">LINEERR_ constant</a> LINEERR_NOMULTIPLEINSTANCE.

The corresponding function at the TAPI level is 
<a href="/windows/desktop/api/tapi/nf-tapi-lineaddprovider">lineAddProvider</a>. The 
<a href="/previous-versions/windows/desktop/legacy/ms725223(v=vs.85)">LINE_CREATE</a> message informs applications that are running about dynamic reconfiguration.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms725223(v=vs.85)">LINE_CREATE</a>



<a href="/previous-versions/windows/desktop/legacy/ms725262(v=vs.85)">PHONE_STATE</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerinit">TSPI_providerInit</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providershutdown">TSPI_providerShutdown</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providerconfig">TUISPI_providerConfig</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providerremove">TUISPI_providerRemove</a>