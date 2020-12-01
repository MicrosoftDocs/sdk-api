---
UID: NF:tapi.phoneGetStatusMessages
title: phoneGetStatusMessages function (tapi.h)
description: The phoneGetStatusMessages function returns which phone-state changes on the specified phone device generate a callback to the application.
helpviewer_keywords: ["_tapi2_phonegetstatusmessages","phoneGetStatusMessages","phoneGetStatusMessages function [TAPI 2.2]","tapi/phoneGetStatusMessages","tapi2.phonegetstatusmessages"]
old-location: tapi2\phonegetstatusmessages.htm
tech.root: tapi3
ms.assetid: 3ee182cf-20e2-4745-9aee-d5de8b44c1b4
ms.date: 12/05/2018
ms.keywords: _tapi2_phonegetstatusmessages, phoneGetStatusMessages, phoneGetStatusMessages function [TAPI 2.2], tapi/phoneGetStatusMessages, tapi2.phonegetstatusmessages
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
 - phoneGetStatusMessages
 - tapi/phoneGetStatusMessages
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
 - phoneGetStatusMessages
---

# phoneGetStatusMessages function


## -description

The 
<b>phoneGetStatusMessages</b> function returns which phone-state changes on the specified phone device generate a callback to the application.

## -parameters

### -param hPhone

Handle to the open phone device to be monitored.

### -param lpdwPhoneStates

Pointer to a <b>DWORD</b> holding zero, one or more of the 
<a href="/windows/desktop/Tapi/phonestate--constants">PHONESTATE_ Constants</a>. These flags specify the set of phone status changes and events for which the application can receive notification messages. Monitoring can be individually enabled and disabled.

### -param lpdwButtonModes

Pointer to a <b>DWORD</b> containing flags that specify the set of phone-button modes for which the application can receive notification messages. This parameter uses zero, one or more of the 
<a href="/windows/desktop/Tapi/phonebuttonmode--constants">PHONEBUTTONMODE_ Constants</a>.

### -param lpdwButtonStates

Pointer to a <b>DWORD</b> that contains flags specifying the set of phone button state changes for which the application can receive notification messages. This parameter uses zero, one or more of the 
<a href="/windows/desktop/Tapi/phonebuttonstate--constants">PHONEBUTTONSTATE_ Constants</a>.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALPOINTER, PHONEERR_RESOURCEUNAVAIL, PHONEERR_OPERATIONFAILED, PHONEERR_UNINITIALIZED.

## -remarks

An application can use 
<b>phoneGetStatusMessages</b> to query the generation of the corresponding messages. Message generation can be controlled by 
<b>phoneGetStatusMessages</b>. All phone status messages are disabled by default.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a>



<a href="/windows/desktop/Tapi/phone-close">PHONE_CLOSE</a>



<a href="/windows/desktop/Tapi/phone-state">PHONE_STATE</a>



<a href="/windows/desktop/Tapi/supplementary-phone-service-functions">Supplementary Phone Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonegetdevcaps">phoneGetDevCaps</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonesetstatusmessages">phoneSetStatusMessages</a>