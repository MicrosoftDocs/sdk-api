---
UID: NF:tspi.TSPI_providerEnumDevices
title: TSPI_providerEnumDevices function (tspi.h)
description: TAPI calls the TSPI_providerEnumDevices function before TSPI_providerInit to determine the number of line and phone devices supported by the service provider.
helpviewer_keywords: ["TSPI_providerEnumDevices","TSPI_providerEnumDevices function [TAPI 2.2]","_tspi_tspi_providerenumdevices","tspi.tspi_providerenumdevices","tspi/TSPI_providerEnumDevices"]
old-location: tspi\tspi_providerenumdevices.htm
tech.root: tapi3
ms.assetid: 5c7c578d-7200-4807-b89b-5bc39ee83e45
ms.date: 12/05/2018
ms.keywords: TSPI_providerEnumDevices, TSPI_providerEnumDevices function [TAPI 2.2], _tspi_tspi_providerenumdevices, tspi.tspi_providerenumdevices, tspi/TSPI_providerEnumDevices
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
 - TSPI_providerEnumDevices
 - tspi/TSPI_providerEnumDevices
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
 - TSPI_providerEnumDevices
---

# TSPI_providerEnumDevices function


## -description

TAPI calls the 
<b>TSPI_providerEnumDevices</b> function before 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerinit">TSPI_providerInit</a> to determine the number of line and phone devices supported by the service provider.

## -parameters

### -param dwPermanentProviderID

The permanent identifier, unique within the service providers on this system, of the service provider being initialized.

### -param lpdwNumLines

A pointer to a <b>DWORD</b>-sized memory location into which the service provider must write the number of line devices it is configured to support. TAPI initializes the value to 0, so if the service provider fails to write a different value, the value 0 is assumed.

### -param lpdwNumPhones

A pointer to a <b>DWORD</b>-sized memory location into which the service provider must write the number of phone devices it is configured to support. TAPI initializes the value to 0, so if the service provider fails to write a different value, the value 0 is assumed.

### -param hProvider

An opaque <b>DWORD</b>-sized value that uniquely identifies this instance of this service provider during this execution of the  Telephony environment.

### -param lpfnLineCreateProc

A pointer to the 
<a href="/windows/desktop/api/tspi/nc-tspi-lineevent">LINEEVENT</a> callback procedure supplied by TAPI. The service provider uses this function to send 
<a href="/previous-versions/windows/desktop/legacy/ms725223(v=vs.85)">LINE_CREATE</a> messages when a new line device needs to be created.

### -param lpfnPhoneCreateProc

A pointer to the 
<a href="/windows/desktop/api/tspi/nc-tspi-phoneevent">PHONEEVENT</a> callback procedure supplied by TAPI. The service provider uses this function to send 
<a href="/previous-versions/windows/desktop/legacy/ms725256(v=vs.85)">PHONE_CREATE</a> messages when a new phone device needs to be created.

## -returns

Returns zero if the request succeeds or an error number if an error occurs. Possible return values are:

LINEERR_NOMEM, LINEERR_OPERATIONFAILED.

## -remarks

In previous versions of TAPI, implementation of this function was optional. Beginning with TAPI 2.0, implementation of this function is mandatory in all service providers. TAPI no longer checks Telephon.ini or the Registry at TAPI startup to determine the initial number of lines and phones supported by a service provider.

A new device can appear prior to the completion of the 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerinit">TSPI_providerInit</a> procedure. TAPI handles properly any _CREATE messages during the provider initialization.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-lineevent">LINEEVENT</a>



<a href="/previous-versions/windows/desktop/legacy/ms725223(v=vs.85)">LINE_CREATE</a>



<a href="/windows/desktop/api/tspi/nc-tspi-phoneevent">PHONEEVENT</a>



<a href="/previous-versions/windows/desktop/legacy/ms725256(v=vs.85)">PHONE_CREATE</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerinit">TSPI_providerInit</a>