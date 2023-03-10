---
UID: NS:tapi.phonemessage_tag
title: PHONEMESSAGE (tapi.h)
description: The PHONEMESSAGE structure contains the next message queued for delivery to the application. The phoneGetMessage function returns this structure.
helpviewer_keywords: ["*LPPHONEMESSAGE","LPPHONEMESSAGE","LPPHONEMESSAGE structure pointer [TAPI 2.2]","PHONEMESSAGE","PHONEMESSAGE structure [TAPI 2.2]","_tapi2_phonemessage_str","tapi/LPPHONEMESSAGE","tapi/PHONEMESSAGE","tapi2.phonemessage_str"]
old-location: tapi2\phonemessage_str.htm
tech.root: tapi3
ms.assetid: 3655efef-d24c-4d67-b1dc-29d1948a1869
ms.date: 12/05/2018
ms.keywords: '*LPPHONEMESSAGE, LPPHONEMESSAGE, LPPHONEMESSAGE structure pointer [TAPI 2.2], PHONEMESSAGE, PHONEMESSAGE structure [TAPI 2.2], _tapi2_phonemessage_str, tapi/LPPHONEMESSAGE, tapi/PHONEMESSAGE, tapi2.phonemessage_str'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PHONEMESSAGE, *LPPHONEMESSAGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - phonemessage_tag
 - tapi/phonemessage_tag
 - LPPHONEMESSAGE
 - tapi/LPPHONEMESSAGE
 - PHONEMESSAGE
 - tapi/PHONEMESSAGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - PHONEMESSAGE
---

# PHONEMESSAGE structure


## -description

The 
<b>PHONEMESSAGE</b> structure contains the next message queued for delivery to the application. The 
<a href="/windows/desktop/api/tapi/nf-tapi-phonegetmessage">phoneGetMessage</a> function returns this structure.

## -struct-fields

### -field hDevice

Handle to a phone device.

### -field dwMessageID

Phone message.

### -field dwCallbackInstance

Instance data passed back to the application, which was specified by the application in 
<a href="/windows/desktop/api/tapi/nf-tapi-phoneinitializeexa">phoneInitializeEx</a>. This value is not interpreted by TAPI.

### -field dwParam1

Parameter for the message.

### -field dwParam2

Parameter for the message.

### -field dwParam3

Parameter for the message.

## -remarks

For information about parameter values passed in this structure, see 
<a href="/windows/desktop/Tapi/phone-device-messages">Phone Device Messages</a>.

## -see-also

<a href="/windows/desktop/api/tapi/nf-tapi-phonegetmessage">phoneGetMessage</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phoneinitializeexa">phoneInitializeEx</a>