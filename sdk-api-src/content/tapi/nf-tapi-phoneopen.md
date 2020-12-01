---
UID: NF:tapi.phoneOpen
title: phoneOpen function (tapi.h)
description: The phoneOpen function opens the specified phone device.
helpviewer_keywords: ["_tapi2_phoneopen","phoneOpen","phoneOpen function [TAPI 2.2]","tapi/phoneOpen","tapi2.phoneopen"]
old-location: tapi2\phoneopen.htm
tech.root: tapi3
ms.assetid: 8fba6d5e-0d8c-488f-a17c-4852b487e300
ms.date: 12/05/2018
ms.keywords: _tapi2_phoneopen, phoneOpen, phoneOpen function [TAPI 2.2], tapi/phoneOpen, tapi2.phoneopen
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
 - phoneOpen
 - tapi/phoneOpen
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
 - phoneOpen
---

# phoneOpen function


## -description

The 
<b>phoneOpen</b> function opens the specified phone device. A phone device can be opened using either owner privilege or monitor privilege. An application that opens the phone with owner privilege can control the phone's lamps, display, ringer, and hookswitch or hookswitches. An application that opens the phone device with monitor privilege is notified only about events that occur at the phone, such as hookswitch changes or button presses.

Ownership of a phone device is exclusive. In other words, only one application can have a phone device opened with owner privilege at a time. The phone device can, however, be opened multiple times with monitor privilege.

## -parameters

### -param hPhoneApp

Handle to the application's registration with TAPI.

### -param dwDeviceID

Identifier of the phone device to be opened.

### -param lphPhone

Pointer to an HPHONE handle that identifies the open phone device. Use this handle to identify the device when invoking other phone control functions.

### -param dwAPIVersion

API version number under which the application and Telephony API have agreed to operate. This number is obtained from 
<a href="/windows/desktop/api/tapi/nf-tapi-phonenegotiateapiversion">phoneNegotiateAPIVersion</a>.

### -param dwExtVersion

Extension version number under which the application and the service provider agree to operate. This number is zero if the application does not use any extensions. This number is obtained from 
<a href="/windows/desktop/api/tapi/nf-tapi-phonenegotiateextversion">phoneNegotiateExtVersion</a>.

### -param dwCallbackInstance

User instance data passed back to the application with each message. This parameter is not interpreted by the Telephony API.

### -param dwPrivilege

Privilege requested. This parameter uses one and only one of the 
<a href="/windows/desktop/Tapi/phoneprivilege--constants">PHONEPRIVILEGE_ Constants</a>.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_ALLOCATED, PHONEERR_NODRIVER, PHONEERR_BADDEVICEID, PHONEERR_NOMEM, PHONEERR_INCOMPATIBLEAPIVERSION, PHONEERR_OPERATIONFAILED, PHONEERR_INCOMPATIBLEEXTVERSION, PHONEERR_OPERATIONUNAVAIL, PHONEERR_INVALAPPHANDLE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPOINTER, PHONEERR_UNINITIALIZED, PHONEERR_INVALPRIVILEGE, PHONEERR_REINIT, PHONEERR_INUSE, PHONEERR_NODEVICE, PHONEERR_INIFILECORRUPT.

## -remarks

When opening a phone device with monitor privileges, the application is sent messages when events occur that change the status of the phone. Messages sent to the application include 
<a href="/windows/desktop/Tapi/phone-button">PHONE_BUTTON</a> and 
<a href="/windows/desktop/Tapi/phone-state">PHONE_STATE</a>. The latter provides an indication of the phone's status item that has changed.

When opening a phone with owner privilege, the phone device can be manipulated in ways that affect the state of the phone device. An application should only open a phone using owner privilege if it actively wants to manipulate the phone device, and it should close the phone device when finished to allow other applications to control the phone.

When an application opens a phone device, it must specify the negotiated API version and, if it wants to use the phone's extensions, the phone's device-specific extension version. This version number should have been obtained with the 
<a href="/windows/desktop/api/tapi/nf-tapi-phonenegotiateapiversion">phoneNegotiateAPIVersion</a> and 
<a href="/windows/desktop/api/tapi/nf-tapi-phonenegotiateextversion">phoneNegotiateExtVersion</a> functions. Version numbering allows the mix and match of different application versions with different API versions and service-provider versions.

## -see-also

<a href="/windows/desktop/Tapi/phone-button">PHONE_BUTTON</a>



<a href="/windows/desktop/Tapi/phone-state">PHONE_STATE</a>



<a href="/windows/desktop/Tapi/supplementary-phone-service-functions">Supplementary Phone Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonenegotiateapiversion">phoneNegotiateAPIVersion</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonenegotiateextversion">phoneNegotiateExtVersion</a>