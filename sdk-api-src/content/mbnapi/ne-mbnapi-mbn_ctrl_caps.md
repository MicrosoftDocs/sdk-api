---
UID: NE:mbnapi.MBN_CTRL_CAPS
title: MBN_CTRL_CAPS (mbnapi.h)
author: windows-sdk-content
description: The MBN_CTRL_CAPS enumerated type represents all of the Mobile Broadband device control capabilities as bit fields.
old-location: mbn\mbn_ctrl_caps.htm
tech.root: mbn
ms.assetid: c4c4bb3b-76ce-4872-8ea1-d2839cbc9b1b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MBN_CTRL_CAPS, MBN_CTRL_CAPS enumeration [Microsoft Broadband Networks], MBN_CTRL_CAPS_CDMA_MOBILE_IP, MBN_CTRL_CAPS_CDMA_SIMPLE_IP, MBN_CTRL_CAPS_HW_RADIO_SWITCH, MBN_CTRL_CAPS_MODEL_MULTI_CARRIER, MBN_CTRL_CAPS_MULTI_MODE, MBN_CTRL_CAPS_NONE, MBN_CTRL_CAPS_PROTECT_UNIQUEID, MBN_CTRL_CAPS_REG_MANUAL, MBN_CTRL_CAPS_USSD, mbn.mbn_ctrl_caps, mbnapi/MBN_CTRL_CAPS, mbnapi/MBN_CTRL_CAPS_CDMA_MOBILE_IP, mbnapi/MBN_CTRL_CAPS_CDMA_SIMPLE_IP, mbnapi/MBN_CTRL_CAPS_HW_RADIO_SWITCH, mbnapi/MBN_CTRL_CAPS_MODEL_MULTI_CARRIER, mbnapi/MBN_CTRL_CAPS_MULTI_MODE, mbnapi/MBN_CTRL_CAPS_NONE, mbnapi/MBN_CTRL_CAPS_PROTECT_UNIQUEID, mbnapi/MBN_CTRL_CAPS_REG_MANUAL, mbnapi/MBN_CTRL_CAPS_USSD
ms.topic: enum
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - mbnapi.h
api_name:
 - MBN_CTRL_CAPS
product: Windows
targetos: Windows
req.typenames: MBN_CTRL_CAPS
req.redist: 
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

