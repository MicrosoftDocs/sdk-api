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

# MBN_CTRL_CAPS enumeration


## -description


The <b>MBN_CTRL_CAPS</b> enumerated type represents all of the Mobile Broadband device control capabilities as bit fields.


## -enum-fields




### -field MBN_CTRL_CAPS_NONE

Device control capabilities are unavailable.


### -field MBN_CTRL_CAPS_REG_MANUAL

Manual selection is allowed for the interface.  This field will not be set for CDMA type interfaces.


### -field MBN_CTRL_CAPS_HW_RADIO_SWITCH

Hardware radio switch functionality is supported.


### -field MBN_CTRL_CAPS_CDMA_MOBILE_IP

The Mobile Broadband device is configured for Mobile IP support.  This field is applicable only to CDMA devices.


### -field MBN_CTRL_CAPS_CDMA_SIMPLE_IP

The Mobile Broadband device is configured for Simple IP support.  This field is applicable only to CDMA devices.

If this field is set in conjunction with <b>MBN_CTRL_CAPS_MOBILE_IP</b>, then this indicates that the device is configured for Mobile IP with Simple IP as a fallback option.


### -field MBN_CTRL_CAPS_PROTECT_UNIQUEID

In some countries or regions, showing the International Mobile Subscriber Identity (IMSI) to the user is not allowed. When this flag is set, the application should not display the IMSI to users.


### -field MBN_CTRL_CAPS_MODEL_MULTI_CARRIER

Windows 8 or later: The Mobile Broadband device supports multi-carrier functionality and is not restricted by a Network Service Provider (NSP).


### -field MBN_CTRL_CAPS_USSD

Windows 8 or later: The Mobile Broadband device supports the USSD protocol. This flag applies only to GSM-based devices.


### -field MBN_CTRL_CAPS_MULTI_MODE

Windows 8 or later: The Mobile Broadband device supports multiple cellular classes.

