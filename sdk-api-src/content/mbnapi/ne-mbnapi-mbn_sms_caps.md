---
UID: NE:mbnapi.MBN_SMS_CAPS
title: MBN_SMS_CAPS
author: windows-sdk-content
description: The MBN_SMS_CAPS enumerated type contains bitfield values that specify SMS capabilities.
old-location: mbn\mbn_sms_caps.htm
tech.root: mbn
ms.assetid: 0fb78ef8-2f46-4bee-9340-68c5043bf9a4
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: MBN_SMS_CAPS, MBN_SMS_CAPS enumeration [Microsoft Broadband Networks], MBN_SMS_CAPS_NONE, MBN_SMS_CAPS_PDU_RECEIVE, MBN_SMS_CAPS_PDU_SEND, MBN_SMS_CAPS_TEXT_RECEIVE, MBN_SMS_CAPS_TEXT_SEND, mbn.mbn_sms_caps, mbnapi/MBN_SMS_CAPS, mbnapi/MBN_SMS_CAPS_NONE, mbnapi/MBN_SMS_CAPS_PDU_RECEIVE, mbnapi/MBN_SMS_CAPS_PDU_SEND, mbnapi/MBN_SMS_CAPS_TEXT_RECEIVE, mbnapi/MBN_SMS_CAPS_TEXT_SEND
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - MBN_SMS_CAPS
product: Windows
targetos: Windows
req.typenames: MBN_SMS_CAPS
req.redist: 
---

# MBN_SMS_CAPS enumeration


## -description


The <b>MBN_SMS_CAPS</b> enumerated type contains bitfield values that specify  SMS capabilities.

These enumerated values are used by the <b>smsCaps</b> member of the <a href="https://msdn.microsoft.com/faee7f53-b465-4240-b163-ce88fae764df">MBN_INTERFACE_CAPS</a> structure.


## -enum-fields




### -field MBN_SMS_CAPS_NONE

The device does not support SMS.


### -field MBN_SMS_CAPS_PDU_RECEIVE

For GSM devices, this indicates that the device is capable of receiving PDU-type SMS. 
For CDMA devices, this indicates that the device is capable of reading the SMS in binary format as defined in â€œsection 3.4.2.1 SMS Point-to-Point Messageâ€ in 3GPP2 specification C.S0015-A â€œShort Message Service (SMS) for Wideband Spread Spectrum Systemsâ€.


### -field MBN_SMS_CAPS_PDU_SEND

For GSM devices, this indicates that the device is capable of sending PDU-type SMS. 
For CDMA devices, this indicates that the device is capable of sending the SMS in binary format as defined in â€œsection 3.4.2.1 SMS Point-to-Point Messageâ€ in 3GPP2 specification C.S0015-A â€œShort Message Service (SMS) for Wideband Spread Spectrum Systemsâ€.


### -field MBN_SMS_CAPS_TEXT_RECEIVE

The device supports  receiving text-type SMS messages.  This is applicable only to CDMA devices.


### -field MBN_SMS_CAPS_TEXT_SEND

The device supports  sending text-type SMS messages.  This is applicable only to CDMA devices.

