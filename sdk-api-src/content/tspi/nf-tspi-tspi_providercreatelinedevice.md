---
UID: NF:tspi.TSPI_providerCreateLineDevice
title: TSPI_providerCreateLineDevice function (tspi.h)
description: The TSPI_providerCreateLineDevice function is called by TAPI in response to receipt of a LINE_CREATE message from the service provider, which allows the dynamic creation of a new line device.
helpviewer_keywords: ["TSPI_providerCreateLineDevice","TSPI_providerCreateLineDevice function [TAPI 2.2]","_tspi_tspi_providercreatelinedevice","tspi.tspi_providercreatelinedevice","tspi/TSPI_providerCreateLineDevice"]
old-location: tspi\tspi_providercreatelinedevice.htm
tech.root: tapi3
ms.assetid: 58c28934-7c2f-49ec-af40-b32b05ec921a
ms.date: 12/05/2018
ms.keywords: TSPI_providerCreateLineDevice, TSPI_providerCreateLineDevice function [TAPI 2.2], _tspi_tspi_providercreatelinedevice, tspi.tspi_providercreatelinedevice, tspi/TSPI_providerCreateLineDevice
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
 - TSPI_providerCreateLineDevice
 - tspi/TSPI_providerCreateLineDevice
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
 - TSPI_providerCreateLineDevice
---

# TSPI_providerCreateLineDevice function


## -description

The 
<b>TSPI_providerCreateLineDevice</b> function is called by TAPI in response to receipt of a 
<a href="/previous-versions/windows/desktop/legacy/ms725223(v=vs.85)">LINE_CREATE</a> message from the service provider, which allows the dynamic creation of a new line device.

## -parameters

### -param dwTempID

The temporary device identifier that the service provider passed to TAPI in the 
<a href="/previous-versions/windows/desktop/legacy/ms725223(v=vs.85)">LINE_CREATE</a> message.

### -param dwDeviceID

The device identifier that TAPI assigns to this device if this function succeeds.

## -returns

Returns zero if the request succeeds or an error number if an error occurs. Possible return values are:

LINEERR_BADDEVICEID, LINEERR_NOMEM, LINEERR_OPERATIONFAILED.

## -remarks

When TAPI receives a 
<a href="/previous-versions/windows/desktop/legacy/ms725223(v=vs.85)">LINE_CREATE</a> message from a service provider, it calls this function (it never calls this function spontaneously). TAPI adds 1 to the number of devices of that type, and passes the resulting new, unused device identifier as the <i>dwDeviceID</i> parameter to this function. It also passes in the function the <i>dwParam2</i> parameter from the LINE_CREATE message as <i>dwTempID</i>.

<div class="alert"><b>Note</b>  Adding the new device to the end of the device list is likely to produce noncontiguous device identifiers for the service provider; service providers that support dynamic device creation must also support noncontiguous device identifiers.</div>
<div> </div>
If the service provider recognizes the <i>dwTempID</i> and succeeds in setting up the structures and such that it needs to support the new device, it saves off the <i>dwDeviceID</i>, and returns SUCCESS. If this function is unsuccessful, TAPI doesn't add the device, and there are no negative effects (the 
<a href="/previous-versions/windows/desktop/legacy/ms725223(v=vs.85)">LINE_CREATE</a> message is ignored). If this function completes successfully, TAPI then informs applications of the availability of the new device using LINE_CREATE or 
<a href="/previous-versions/windows/desktop/legacy/ms725231(v=vs.85)">LINE_LINEDEVSTATE</a> (LINEDEVSTATE_REINIT) messages.

Older service providers that do not export this function, however, also should not send LINE_CREATE messages, which means TAPI would not try to call this function.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms725223(v=vs.85)">LINE_CREATE</a>



<a href="/previous-versions/windows/desktop/legacy/ms725231(v=vs.85)">LINE_LINEDEVSTATE</a>