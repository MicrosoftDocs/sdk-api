---
UID: NF:tspi.TSPI_providerConfig
title: TSPI_providerConfig function (tspi.h)
description: The TSPI_providerConfig function is obsolete. TAPI version 1.4 or earlier service providers can implement this TSPI function. TAPI version 2.0 or later TSPs implement TUISPI_providerConfig.
helpviewer_keywords: ["TSPI_providerConfig","TSPI_providerConfig function [TAPI 2.2]","_tspi_tspi_providerconfig","tspi.tspi_providerconfig","tspi/TSPI_providerConfig"]
old-location: tspi\tspi_providerconfig.htm
tech.root: tapi3
ms.assetid: b0fa2a9e-bc8b-4364-9442-2091f2366107
ms.date: 12/05/2018
ms.keywords: TSPI_providerConfig, TSPI_providerConfig function [TAPI 2.2], _tspi_tspi_providerconfig, tspi.tspi_providerconfig, tspi/TSPI_providerConfig
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
 - TSPI_providerConfig
 - tspi/TSPI_providerConfig
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
 - TSPI_providerConfig
---

# TSPI_providerConfig function


## -description

The 
<b>TSPI_providerConfig</b> function is obsolete. TAPI version 1.4 or earlier service providers can implement this TSPI function. TAPI version 2.0 or later TSPs implement 
<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providerconfig">TUISPI_providerConfig</a>.

The 
<b>TSPI_providerConfig</b> function gathers configuration information from the user. It may use a dialog box, and this dialog box can include sub-dialog boxes associated with other APIs (such as Comm/datamodem) for the setup of specific devices.

## -parameters

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

The Telephony Control Panel utility supplied with Windows Telephony in versions 1.4 and earlier calls this function when the setup command is invoked.

There is no directly corresponding function at the TAPI level. In TAPI, applications have access to the functions 
<a href="/windows/desktop/api/tapi/nf-tapi-lineconfigdialog">lineConfigDialog</a> and 
<a href="/windows/desktop/api/tapi/nf-tapi-phoneconfigdialog">phoneConfigDialog</a>, which allow configuration of parameters of a particular line or phone once it has been installed.

## -see-also

<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineconfigdialog">TSPI_lineConfigDialog</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phoneconfigdialog">TSPI_phoneConfigDialog</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerinstall">TSPI_providerInstall</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerremove">TSPI_providerRemove</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providerconfig">TUISPI_providerConfig</a>