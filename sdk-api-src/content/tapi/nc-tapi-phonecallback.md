---
UID: NC:tapi.PHONECALLBACK
title: PHONECALLBACK (tapi.h)
description: The phoneCallback function is a placeholder for the application-supplied function name.
helpviewer_keywords: ["PHONECALLBACK","PHONECALLBACK callback function [TAPI 2.2]","_tapi2_phonecallbackfunc","phoneCallback","phoneCallback callback","tapi/PHONECALLBACK","tapi2.phonecallbackfunc"]
old-location: tapi2\phonecallbackfunc.htm
tech.root: tapi3
ms.assetid: 169ac08a-7584-4d43-abb3-eb83eeb48406
ms.date: 12/05/2018
ms.keywords: PHONECALLBACK, PHONECALLBACK callback function [TAPI 2.2], _tapi2_phonecallbackfunc, phoneCallback, phoneCallback callback, tapi/PHONECALLBACK, tapi2.phonecallbackfunc
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PHONECALLBACK
 - tapi/PHONECALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tapi.h
api_name:
 - PHONECALLBACK
---

# PHONECALLBACK callback function


## -description

The 
<b>phoneCallback</b> function is a placeholder for the application-supplied function name.

## -parameters

### -param hDevice

Handle to a phone device associated with the callback.

### -param dwMessage

### -param dwInstance

### -param dwParam1

Parameter for the message.

### -param dwParam2

Parameter for the message.

### -param dwParam3

Parameter for the message.


#### - dwCallbackInstance

Callback instance data passed back to the application in the callback. This <b>DWORD</b> is not interpreted by TAPI.


#### - dwMsg

Line or call device message.

## -remarks

For more information about the parameters passed to this callback function, see 
<a href="/windows/desktop/Tapi/tapi-messages">TAPI Messages</a>.

All callbacks occur in the application's context. The callback function must reside in a dynamic-link library (DLL) or application module and be exported in the module-definition file.