---
UID: NF:tspi.TUISPI_providerConfig
title: TUISPI_providerConfig function (tspi.h)
description: The TUISPI_providerConfig function implements the UI elements that must execute in the context of the calling application. This function makes the TSPI_providerConfig function obsolete in version 2.0 and later (supported in version 1.4 and earlier).
helpviewer_keywords: ["TUISPI_providerConfig","TUISPI_providerConfig function [TAPI 2.2]","_tspi_tuispi_providerconfig","tspi.tuispi_providerconfig","tspi/TUISPI_providerConfig"]
old-location: tspi\tuispi_providerconfig.htm
tech.root: tapi3
ms.assetid: 9730f61a-8da7-4693-9fd2-94650e36ce8a
ms.date: 12/05/2018
ms.keywords: TUISPI_providerConfig, TUISPI_providerConfig function [TAPI 2.2], _tspi_tuispi_providerconfig, tspi.tuispi_providerconfig, tspi/TUISPI_providerConfig
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
 - TUISPI_providerConfig
 - tspi/TUISPI_providerConfig
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
 - TUISPI_providerConfig
---

# TUISPI_providerConfig function


## -description

The 
<b>TUISPI_providerConfig</b> function implements the UI elements that must execute in the context of the calling application. This function makes the 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerconfig">TSPI_providerConfig</a> function obsolete in version 2.0 and later (supported in version 1.4 and earlier).

The 
<b>TUISPI_providerConfig</b> function gathers configuration information from the user. It can use a dialog box, and this dialog box can include sub-dialog boxes associated with other APIs (such as Comm/datamodem) for the setup of specific devices.

Implementation is optional.

## -parameters

### -param lpfnUIDLLCallback

Pointer to a function the UI DLL can call to communicate with the service provider DLL to obtain information needed to display the dialog box and to send updated configuration to the service provider.

### -param hwndOwner

The handle of the parent window in which the function can create any dialog box windows required during the configuration.

### -param dwPermanentProviderID

The service provider's permanent provider identifier.

## -returns

Returns zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_OPERATIONFAILED, LINEERR_NOMEM.

## -remarks

This function may be called while the service provider is in use (that is, between calls of 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerinit">TSPI_providerInit</a> and 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providershutdown">TSPI_providerShutdown</a>).

Any changes that affect the behavior visible through TSPI should take effect only when the service provider is restarted at the next 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerinit">TSPI_providerInit</a>.

There is no directly corresponding function at the TAPI level. In TAPI, applications have access to the functions 
<a href="/windows/desktop/api/tapi/nf-tapi-lineconfigdialog">lineConfigDialog</a> and 
<a href="/windows/desktop/api/tapi/nf-tapi-phoneconfigdialog">phoneConfigDialog</a>, which allow configuration of parameters of a particular line or phone once it has been installed.

## -see-also

<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_lineconfigdialog">TUISPI_lineConfigDialog</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_phoneconfigdialog">TUISPI_phoneConfigDialog</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providerinstall">TUISPI_providerInstall</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providerremove">TUISPI_providerRemove</a>