---
UID: NF:tspi.TSPI_phoneGetHookSwitch
title: TSPI_phoneGetHookSwitch function (tspi.h)
description: The TSPI_phoneGetHookSwitch function returns the current hookswitch mode of the specified open phone device.
helpviewer_keywords: ["TSPI_phoneGetHookSwitch","TSPI_phoneGetHookSwitch function [TAPI 2.2]","_tspi_tspi_phonegethookswitch","tspi.tspi_phonegethookswitch","tspi/TSPI_phoneGetHookSwitch"]
old-location: tspi\tspi_phonegethookswitch.htm
tech.root: tapi3
ms.assetid: 31248a74-84f2-4ca6-a6fc-f8710953ce34
ms.date: 12/05/2018
ms.keywords: TSPI_phoneGetHookSwitch, TSPI_phoneGetHookSwitch function [TAPI 2.2], _tspi_tspi_phonegethookswitch, tspi.tspi_phonegethookswitch, tspi/TSPI_phoneGetHookSwitch
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
 - TSPI_phoneGetHookSwitch
 - tspi/TSPI_phoneGetHookSwitch
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
 - TSPI_phoneGetHookSwitch
---

# TSPI_phoneGetHookSwitch function


## -description

The 
<b>TSPI_phoneGetHookSwitch</b> function returns the current hookswitch mode of the specified open phone device.

## -parameters

### -param hdPhone

The service provider's opaque handle to the phone whose hookswitch mode is to be retrieved.

### -param lpdwHookSwitchDevs

A pointer to a <b>DWORD</b>-sized location into which the service provider writes the mode of the phone's hookswitch devices. This parameter uses one of the 
<a href="/windows/desktop/Tapi/phonehookswitchdev--constants">PHONEHOOKSWITCHDEV_ constants</a>. If a bit position is <b>FALSE</b>, the corresponding hookswitch device is onhook. If <b>TRUE</b>, the microphone and/or speaker part of the corresponding hookswitch device is offhook. To find out whether microphone and/or speaker are enabled, TAPI can use 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetstatus">TSPI_phoneGetStatus</a>.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_NOMEM, PHONEERR_OPERATIONUNAVAIL.

## -remarks

After the hookswitch state of a device changes, and if hookswitch monitoring is enabled, TAPI is sent a PHONE_STATE message.

## -see-also

<a href="/windows/desktop/Tapi/phonehookswitchdev--constants">PHONEHOOKSWITCHDEV_ Constants</a>



<a href="/windows/desktop/api/tapi/ns-tapi-phonestatus">PHONESTATUS</a>



<a href="/previous-versions/windows/desktop/legacy/ms725262(v=vs.85)">PHONE_STATE</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetstatus">TSPI_phoneGetStatus</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonesethookswitch">TSPI_phoneSetHookSwitch</a>