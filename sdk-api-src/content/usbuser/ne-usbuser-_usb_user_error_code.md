---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

