---
UID: NF:tapi.phoneSetStatusMessages
title: phoneSetStatusMessages function (tapi.h)
description: The phoneSetStatusMessages function enables an application to monitor the specified phone device for selected status events.
helpviewer_keywords: ["_tapi2_phonesetstatusmessages","phoneSetStatusMessages","phoneSetStatusMessages function [TAPI 2.2]","tapi/phoneSetStatusMessages","tapi2.phonesetstatusmessages"]
old-location: tapi2\phonesetstatusmessages.htm
tech.root: tapi3
ms.assetid: eb3b6ea8-447f-44df-a0fb-9ab50d6471f8
ms.date: 12/05/2018
ms.keywords: _tapi2_phonesetstatusmessages, phoneSetStatusMessages, phoneSetStatusMessages function [TAPI 2.2], tapi/phoneSetStatusMessages, tapi2.phonesetstatusmessages
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
 - phoneSetStatusMessages
 - tapi/phoneSetStatusMessages
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
 - phoneSetStatusMessages
---

# phoneSetStatusMessages function


## -description

The 
<b>phoneSetStatusMessages</b> function enables an application to monitor the specified phone device for selected status events.

## -parameters

### -param hPhone

Handle to the open phone device to be monitored.

### -param dwPhoneStates

Set of phone status changes and events for which the application can receive notification messages. This parameter can have zero, one, or more of the 
<a href="/windows/desktop/Tapi/phonestate--constants">PHONESTATE_ Constants</a>.

### -param dwButtonModes

Set of phone-button modes for which the application can receive notification messages. This parameter can have zero, one, or more of the 
<a href="/windows/desktop/Tapi/phonebuttonmode--constants">PHONEBUTTONMODE_ Constants</a>.

### -param dwButtonStates

Set of phone-button state changes for which the application can receive notification messages. If the <i>dwButtonModes</i> parameter is zero, <i>dwButtonStates</i> is ignored. If <i>dwButtonModes</i> has one or more bits set, this parameter must also have at least one bit set. This parameter uses the 
<a href="/windows/desktop/Tapi/phonebuttonstate--constants">PHONEBUTTONSTATE_ Constants</a>.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALPHONESTATE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALBUTTONMODE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALBUTTONSTATE, PHONEERR_UNINITIALIZED, PHONEERR_OPERATIONUNAVAIL.

## -remarks

An application can use the 
<b>phoneSetStatusMessages</b> function to enable or disable the generation of the corresponding messages. All phone status messages are disabled by default.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a>



<a href="/windows/desktop/Tapi/phone-close">PHONE_CLOSE</a>



<a href="/windows/desktop/Tapi/phone-state">PHONE_STATE</a>



<a href="/windows/desktop/Tapi/supplementary-phone-service-functions">Supplementary Phone Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonegetdevcaps">phoneGetDevCaps</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phoneinitialize">phoneInitialize</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phoneinitializeexa">phoneInitializeEx</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phoneopen">phoneOpen</a>