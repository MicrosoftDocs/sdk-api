---
UID: NS:tapi.linemessage_tag
title: LINEMESSAGE (tapi.h)
description: The LINEMESSAGE structure contains parameter values specifying a change in status of the line the application currently has open. The lineGetMessage function returns the LINEMESSAGE structure.
helpviewer_keywords: ["*LPLINEMESSAGE","LINEMESSAGE","LINEMESSAGE structure [TAPI 2.2]","LPLINEMESSAGE","LPLINEMESSAGE structure pointer [TAPI 2.2]","_tapi2_linemessage_str","tapi/LINEMESSAGE","tapi/LPLINEMESSAGE","tapi2.linemessage_str"]
old-location: tapi2\linemessage_str.htm
tech.root: tapi3
ms.assetid: 1d184948-4ba2-4c8c-8771-d1aea6c4f565
ms.date: 12/05/2018
ms.keywords: '*LPLINEMESSAGE, LINEMESSAGE, LINEMESSAGE structure [TAPI 2.2], LPLINEMESSAGE, LPLINEMESSAGE structure pointer [TAPI 2.2], _tapi2_linemessage_str, tapi/LINEMESSAGE, tapi/LPLINEMESSAGE, tapi2.linemessage_str'
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
req.typenames: LINEMESSAGE, *LPLINEMESSAGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - linemessage_tag
 - tapi/linemessage_tag
 - LPLINEMESSAGE
 - tapi/LPLINEMESSAGE
 - LINEMESSAGE
 - tapi/LINEMESSAGE
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
 - LINEMESSAGE
---

# LINEMESSAGE structure


## -description

The 
<b>LINEMESSAGE</b> structure contains parameter values specifying a change in status of the line the application currently has open. The 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetmessage">lineGetMessage</a> function returns the 
<b>LINEMESSAGE</b> structure.

## -struct-fields

### -field hDevice

Handle to either a line device or a call. The nature of this handle (line handle or call handle) can be determined by the context provided by <i>dwMessageID</i>.

### -field dwMessageID

Line or call device message.

### -field dwCallbackInstance

Instance data passed back to the application, which was specified by the application in the <i>dwCallBackInstance</i> parameter of 
<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>. This <b>DWORD</b> is not interpreted by TAPI.

### -field dwParam1

Parameter for the message.

### -field dwParam2

Parameter for the message.

### -field dwParam3

Parameter for the message.

## -remarks

For information about parameter values passed in this structure, see 
<a href="/windows/desktop/Tapi/line-device-messages">Line Device Messages</a>.

## -see-also

<a href="/windows/desktop/api/tapi/nf-tapi-linegetmessage">lineGetMessage</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>