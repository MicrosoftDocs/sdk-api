---
UID: NS:tapi.linemessage_tag
title: LINEMESSAGE (tapi.h)
author: windows-sdk-content
description: The LINEMESSAGE structure contains parameter values specifying a change in status of the line the application currently has open. The lineGetMessage function returns the LINEMESSAGE structure.
old-location: tapi2\linemessage_str.htm
tech.root: Tapi
ms.assetid: 1d184948-4ba2-4c8c-8771-d1aea6c4f565
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPLINEMESSAGE, LINEMESSAGE, LINEMESSAGE structure [TAPI 2.2], LPLINEMESSAGE, LPLINEMESSAGE structure pointer [TAPI 2.2], _tapi2_linemessage_str, tapi/LINEMESSAGE, tapi/LPLINEMESSAGE, tapi2.linemessage_str"
ms.topic: struct
f1_keywords: ["tapi/LINEMESSAGE"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEMESSAGE
product: Windows
targetos: Windows
req.typenames: LINEMESSAGE, *LPLINEMESSAGE
req.redist: 
ms.custom: 19H1
---

# LINEMESSAGE structure


## -description


The 
<b>LINEMESSAGE</b> structure contains parameter values specifying a change in status of the line the application currently has open. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linegetmessage">lineGetMessage</a> function returns the 
<b>LINEMESSAGE</b> structure.


## -struct-fields




### -field hDevice

Handle to either a line device or a call. The nature of this handle (line handle or call handle) can be determined by the context provided by <i>dwMessageID</i>.


### -field dwMessageID

Line or call device message.


### -field dwCallbackInstance

Instance data passed back to the application, which was specified by the application in the <i>dwCallBackInstance</i> parameter of 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>. This <b>DWORD</b> is not interpreted by TAPI.


### -field dwParam1

Parameter for the message.


### -field dwParam2

Parameter for the message.


### -field dwParam3

Parameter for the message.


## -remarks



For information about parameter values passed in this structure, see 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/line-device-messages">Line Device Messages</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linegetmessage">lineGetMessage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>
 

 

