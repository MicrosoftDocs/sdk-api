---
UID: NE:usbuser._USB_USER_ERROR_CODE
title: "_USB_USER_ERROR_CODE"
author: windows-sdk-content
description: The USB_USER_ERROR_CODE enumeration lists the error codes that a USB user-mode request reports when it fails.
old-location: buses\usb_user_error_code.htm
old-project: usbref
ms.assetid: 25dab683-70bd-4d3e-8295-d4a670c5b2ed
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: USB_USER_ERROR_CODE, USB_USER_ERROR_CODE enumeration [Buses], UsbUserBufferTooSmall, UsbUserDeviceNotStarted, UsbUserErrorNotMapped, UsbUserFeatureDisabled, UsbUserInvalidHeaderParameter, UsbUserInvalidParameter, UsbUserInvalidRequestCode, UsbUserMiniportError, UsbUserNoDeviceConnected, UsbUserNotSupported, UsbUserSuccess, _USB_USER_ERROR_CODE, buses.usb_user_error_code, usbstrct_c6461beb-3943-46d0-a426-c01cb52b4986.xml, usbuser/USB_USER_ERROR_CODE, usbuser/UsbUserBufferTooSmall, usbuser/UsbUserDeviceNotStarted, usbuser/UsbUserErrorNotMapped, usbuser/UsbUserFeatureDisabled, usbuser/UsbUserInvalidHeaderParameter, usbuser/UsbUserInvalidParameter, usbuser/UsbUserInvalidRequestCode, usbuser/UsbUserMiniportError, usbuser/UsbUserNoDeviceConnected, usbuser/UsbUserNotSupported, usbuser/UsbUserSuccess
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: usbuser.h
req.include-header: Usbuser.h
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
tech.root: 
req.typenames: USB_USER_ERROR_CODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - usbuser.h
api_name:
 - USB_USER_ERROR_CODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _USB_USER_ERROR_CODE enumeration


## -description


The <b>USB_USER_ERROR_CODE</b> enumeration lists the error codes that a USB user-mode request reports when it fails.


## -enum-fields




### -field UsbUserSuccess

The user request succeeded.


### -field UsbUserNotSupported

The user request was not supported.


### -field UsbUserInvalidRequestCode

The user request code was invalid.


### -field UsbUserFeatureDisabled

The feature that was specified by user request is disabled.


### -field UsbUserInvalidHeaderParameter

The user request contains an invalid header parameter.


### -field UsbUserInvalidParameter

The user request contains an invalid parameter.


### -field UsbUserMiniportError

The user request failed because of a miniport driver error.


### -field UsbUserBufferTooSmall

The user request failed because the data buffer was too small.


### -field UsbUserErrorNotMapped

The USB stack could not map the error to one of the errors that are listed in this enumeration.


### -field UsbUserDeviceNotStarted

The device was not started.


### -field UsbUserNoDeviceConnected

The device was not connected.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539322">USB Constants and Enumerations</a>
 

 

