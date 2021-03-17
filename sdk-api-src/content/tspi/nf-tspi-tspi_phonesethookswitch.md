---
UID: NF:tspi.TSPI_phoneSetHookSwitch
title: TSPI_phoneSetHookSwitch function (tspi.h)
description: The TSPI_phoneSetHookSwitch function sets the hook state of the specified open phone's hookswitch devices to the specified mode. Only the hookswitch state of the hookswitch devices listed is affected.
helpviewer_keywords: ["TSPI_phoneSetHookSwitch","TSPI_phoneSetHookSwitch function [TAPI 2.2]","_tspi_tspi_phonesethookswitch","tspi.tspi_phonesethookswitch","tspi/TSPI_phoneSetHookSwitch"]
old-location: tspi\tspi_phonesethookswitch.htm
tech.root: tapi3
ms.assetid: e0cfe1b7-9904-4baf-8801-43bc1a5d05d8
ms.date: 12/05/2018
ms.keywords: TSPI_phoneSetHookSwitch, TSPI_phoneSetHookSwitch function [TAPI 2.2], _tspi_tspi_phonesethookswitch, tspi.tspi_phonesethookswitch, tspi/TSPI_phoneSetHookSwitch
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
 - TSPI_phoneSetHookSwitch
 - tspi/TSPI_phoneSetHookSwitch
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
 - TSPI_phoneSetHookSwitch
---

# TSPI_phoneSetHookSwitch function


## -description

The 
<b>TSPI_phoneSetHookSwitch</b> function sets the hook state of the specified open phone's hookswitch devices to the specified mode. Only the hookswitch state of the hookswitch devices listed is affected.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdPhone

The handle to the phone containing the hookswitch devices whose modes are to be set.

### -param dwHookSwitchDevs

The device(s) whose hookswitch mode is to be set. This parameter uses one of the 
<a href="/windows/desktop/Tapi/phonehookswitchdev--constants">PHONEHOOKSWITCHDEV_ constants</a>.

### -param dwHookSwitchMode

The hookswitch mode to set. This parameter can have only one of the 
<a href="/windows/desktop/Tapi/phonehookswitchmode--constants">PHONEHOOKSWITCHMODE_ constants</a>.

## -returns

Returns <i>dwRequestID</i> or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds or it is an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALHOOKSWITCHDEV, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALHOOKSWITCHMODE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONUNAVAIL.

## -remarks

The hookswitch mode is changed to the indicated setting for all devices specified. If different settings are desired, this function can be invoked multiple times with a different set of parameters. A 
<a href="/previous-versions/windows/desktop/legacy/ms725262(v=vs.85)">PHONE_STATE</a> message is sent to the application after the hookswitch state has changed.

## -see-also

<a href="/windows/desktop/Tapi/phonehookswitchdev--constants">PHONEHOOKSWITCHDEV_ Constants</a>



<a href="/windows/desktop/Tapi/phonehookswitchmode--constants">PHONEHOOKSWITCHMODE_ Constants</a>



<a href="/windows/desktop/api/tapi/ns-tapi-phonestatus">PHONESTATUS</a>



<a href="/previous-versions/windows/desktop/legacy/ms725262(v=vs.85)">PHONE_STATE</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegethookswitch">TSPI_phoneGetHookSwitch</a>