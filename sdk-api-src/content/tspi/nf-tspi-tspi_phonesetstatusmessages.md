---
UID: NF:tspi.TSPI_phoneSetStatusMessages
title: TSPI_phoneSetStatusMessages function (tspi.h)
description: The TSPI_phoneSetStatusMessages function causes the service provider to filter status messages that are not currently of interest to any application.
helpviewer_keywords: ["TSPI_phoneSetStatusMessages","TSPI_phoneSetStatusMessages function [TAPI 2.2]","_tspi_tspi_phonesetstatusmessages","tspi.tspi_phonesetstatusmessages","tspi/TSPI_phoneSetStatusMessages"]
old-location: tspi\tspi_phonesetstatusmessages.htm
tech.root: tapi3
ms.assetid: 19e240e5-ba75-4806-a271-dc87235ba598
ms.date: 12/05/2018
ms.keywords: TSPI_phoneSetStatusMessages, TSPI_phoneSetStatusMessages function [TAPI 2.2], _tspi_tspi_phonesetstatusmessages, tspi.tspi_phonesetstatusmessages, tspi/TSPI_phoneSetStatusMessages
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
 - TSPI_phoneSetStatusMessages
 - tspi/TSPI_phoneSetStatusMessages
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
 - TSPI_phoneSetStatusMessages
---

# TSPI_phoneSetStatusMessages function


## -description

The 
<b>TSPI_phoneSetStatusMessages</b> function causes the service provider to filter status messages that are not currently of interest to any application.

## -parameters

### -param hdPhone

The opaque handle to the phone whose state-change monitoring filter is to be set.

### -param dwPhoneStates

Flags that specify the set of phone status changes and events for which TAPI wants to receive notification messages. This parameter can have zero, one, or more than one of the 
<a href="/windows/desktop/Tapi/phonestate--constants">PHONESTATE_ constants</a>.

### -param dwButtonModes

Flags that specify the set of phone button modes for which TAPI wants to receive notification messages. If <i>dwButtonModes</i> is zero, <i>dwButtonStates</i> is ignored. This parameter can have zero, one, or more than one of the 
<a href="/windows/desktop/Tapi/phonebuttonmode--constants">PHONEBUTTONMODE_ constants</a>. If <i>dwButtonModes</i> has at least one of these flags set, <i>dwButtonStates</i> must also have at least one bit set:

### -param dwButtonStates

This parameter specifies the set of phone button state changes for which TAPI wishes to receive notification messages, one of the 
<a href="/windows/desktop/Tapi/phonebuttonstate--constants">PHONEBUTTONSTATE_ Constants</a>.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALPHONESTATE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALBUTTONMODE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALBUTTONSTATE, PHONEERR_OPERATIONUNAVAIL.

## -remarks

TAPI defines a number of messages that notify applications about events occurring on phones. The sets of all change messages in which all applications are interested can be much smaller than the set of possible messages. This procedure allows TAPI to tell the service provider the reduced set of messages to deliver. The service provider delivers all of the messages it supports, within the specified set. It is permitted to deliver more (they are filtered out by TAPI), but is discouraged from doing so for performance reasons. If TAPI requests delivery of a particular message type that is not produced by the provider, the provider nevertheless accepts the request but simply does not produce the message. All phone status messages except PHONESTATE_REINIT are disabled by default.

## -see-also

<a href="/windows/desktop/Tapi/phonestate--constants">PHONESTATE_ Constants</a>



<a href="/previous-versions/windows/desktop/legacy/ms725254(v=vs.85)">PHONE_BUTTON</a>



<a href="/previous-versions/windows/desktop/legacy/ms725262(v=vs.85)">PHONE_STATE</a>