---
UID: NF:tapi.phoneDevSpecific
title: phoneDevSpecific function (tapi.h)
description: The phoneDevSpecific function is used as a general extension mechanism to enable a Telephony API implementation to provide features not described in the other TAPI functions. The meanings of these extensions are device specific.
helpviewer_keywords: ["_tapi2_phonedevspecific","phoneDevSpecific","phoneDevSpecific function [TAPI 2.2]","tapi/phoneDevSpecific","tapi2.phonedevspecific"]
old-location: tapi2\phonedevspecific.htm
tech.root: tapi3
ms.assetid: 7199b489-bf66-4380-8d1c-73de5aeb7489
ms.date: 12/05/2018
ms.keywords: _tapi2_phonedevspecific, phoneDevSpecific, phoneDevSpecific function [TAPI 2.2], tapi/phoneDevSpecific, tapi2.phonedevspecific
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
 - phoneDevSpecific
 - tapi/phoneDevSpecific
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
 - phoneDevSpecific
---

# phoneDevSpecific function


## -description

The 
<b>phoneDevSpecific</b> function is used as a general extension mechanism to enable a Telephony API implementation to provide features not described in the other TAPI functions. The meanings of these extensions are device specific.

## -parameters

### -param hPhone

Handle to a phone device.

### -param lpParams

Pointer to a memory area used to hold a parameter block. Its interpretation is device specific. The contents of the parameter block are passed unchanged to or from the service provider by TAPI.

### -param dwSize

Size of the parameter block area, in bytes.

## -returns

Returns a positive request identifier if the function is completed asynchronously or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/phone-reply">PHONE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALPOINTER, PHONEERR_RESOURCEUNAVAIL, PHONEERR_OPERATIONUNAVAIL, PHONEERR_UNINITIALIZED, PHONEERR_OPERATIONFAILED.

Additional return values are device specific.

## -remarks

This operation provides a generic parameter profile. The interpretation of the parameter block is device specific. Indications and replies that are device specific should use the 
<a href="/windows/desktop/Tapi/phone-devspecific">PHONE_DEVSPECIFIC</a> message.

A service provider can provide access to device-specific functions by defining parameters for use with this operation. Applications that want to make use of these device-specific extensions should consult the device-specific (vendor-specific) documentation that describes which extensions are defined. Typically, an application that relies on these device-specific extensions is not portable to work with other service-provider environments.

## -see-also

<a href="/windows/desktop/Tapi/extended-telephony-services-reference">Extended Telephony Services Reference</a>



<a href="/windows/desktop/Tapi/phone-devspecific">PHONE_DEVSPECIFIC</a>



<a href="/windows/desktop/Tapi/phone-reply">PHONE_REPLY</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>