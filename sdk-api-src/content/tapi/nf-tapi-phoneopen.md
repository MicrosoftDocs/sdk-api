---
UID: NF:tapi.phoneOpen
title: phoneOpen function
author: windows-driver-content
description: The phoneOpen function opens the specified phone device.
old-location: tapi2\phoneopen.htm
old-project: Tapi
ms.assetid: 8fba6d5e-0d8c-488f-a17c-4852b487e300
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: "_tapi2_phoneopen, phoneOpen, phoneOpen function [TAPI 2.2], tapi/phoneOpen, tapi2.phoneopen"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: FLICK_POINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Tapi32.dll
api_name:
-	phoneOpen
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
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
<a href="https://msdn.microsoft.com/50c2c15c-459f-451b-9b79-9118acc81c8c">phoneNegotiateAPIVersion</a>.


### -param dwExtVersion

Extension version number under which the application and the service provider agree to operate. This number is zero if the application does not use any extensions. This number is obtained from 
<a href="https://msdn.microsoft.com/f62aa1da-7256-400a-998d-4c24d01989ec">phoneNegotiateExtVersion</a>.


### -param dwCallbackInstance

User instance data passed back to the application with each message. This parameter is not interpreted by the Telephony API.


### -param dwPrivilege

Privilege requested. This parameter uses one and only one of the 
<a href="https://msdn.microsoft.com/1dc2fab9-b044-4ae3-8c16-fa450f9ef714">PHONEPRIVILEGE_ Constants</a>.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_ALLOCATED, PHONEERR_NODRIVER, PHONEERR_BADDEVICEID, PHONEERR_NOMEM, PHONEERR_INCOMPATIBLEAPIVERSION, PHONEERR_OPERATIONFAILED, PHONEERR_INCOMPATIBLEEXTVERSION, PHONEERR_OPERATIONUNAVAIL, PHONEERR_INVALAPPHANDLE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPOINTER, PHONEERR_UNINITIALIZED, PHONEERR_INVALPRIVILEGE, PHONEERR_REINIT, PHONEERR_INUSE, PHONEERR_NODEVICE, PHONEERR_INIFILECORRUPT.




## -remarks



When opening a phone device with monitor privileges, the application is sent messages when events occur that change the status of the phone. Messages sent to the application include 
<a href="https://msdn.microsoft.com/fe47eed7-89d1-488b-b945-9e1aedc1f63c">PHONE_BUTTON</a> and 
<a href="https://msdn.microsoft.com/74e74b62-8387-4056-83e6-2350b3da4077">PHONE_STATE</a>. The latter provides an indication of the phone's status item that has changed.

When opening a phone with owner privilege, the phone device can be manipulated in ways that affect the state of the phone device. An application should only open a phone using owner privilege if it actively wants to manipulate the phone device, and it should close the phone device when finished to allow other applications to control the phone.

When an application opens a phone device, it must specify the negotiated API version and, if it wants to use the phone's extensions, the phone's device-specific extension version. This version number should have been obtained with the 
<a href="https://msdn.microsoft.com/50c2c15c-459f-451b-9b79-9118acc81c8c">phoneNegotiateAPIVersion</a> and 
<a href="https://msdn.microsoft.com/f62aa1da-7256-400a-998d-4c24d01989ec">phoneNegotiateExtVersion</a> functions. Version numbering allows the mix and match of different application versions with different API versions and service-provider versions.




## -see-also




<a href="https://msdn.microsoft.com/fe47eed7-89d1-488b-b945-9e1aedc1f63c">PHONE_BUTTON</a>



<a href="https://msdn.microsoft.com/74e74b62-8387-4056-83e6-2350b3da4077">PHONE_STATE</a>



<a href="https://msdn.microsoft.com/0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5">Supplementary Phone Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/50c2c15c-459f-451b-9b79-9118acc81c8c">phoneNegotiateAPIVersion</a>



<a href="https://msdn.microsoft.com/f62aa1da-7256-400a-998d-4c24d01989ec">phoneNegotiateExtVersion</a>
 

 

