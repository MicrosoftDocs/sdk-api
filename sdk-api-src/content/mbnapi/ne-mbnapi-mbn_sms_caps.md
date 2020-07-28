---
UID: NE:mbnapi.MBN_SMS_CAPS
title: MBN_SMS_CAPS (mbnapi.h)
description: The MBN_SMS_CAPS enumerated type contains bitfield values that specify SMS capabilities.
helpviewer_keywords: ["MBN_SMS_CAPS","MBN_SMS_CAPS enumeration [Microsoft Broadband Networks]","MBN_SMS_CAPS_NONE","MBN_SMS_CAPS_PDU_RECEIVE","MBN_SMS_CAPS_PDU_SEND","MBN_SMS_CAPS_TEXT_RECEIVE","MBN_SMS_CAPS_TEXT_SEND","mbn.mbn_sms_caps","mbnapi/MBN_SMS_CAPS","mbnapi/MBN_SMS_CAPS_NONE","mbnapi/MBN_SMS_CAPS_PDU_RECEIVE","mbnapi/MBN_SMS_CAPS_PDU_SEND","mbnapi/MBN_SMS_CAPS_TEXT_RECEIVE","mbnapi/MBN_SMS_CAPS_TEXT_SEND"]
old-location: mbn\mbn_sms_caps.htm
tech.root: mbn
ms.assetid: 0fb78ef8-2f46-4bee-9340-68c5043bf9a4
ms.date: 12/05/2018
ms.keywords: MBN_SMS_CAPS, MBN_SMS_CAPS enumeration [Microsoft Broadband Networks], MBN_SMS_CAPS_NONE, MBN_SMS_CAPS_PDU_RECEIVE, MBN_SMS_CAPS_PDU_SEND, MBN_SMS_CAPS_TEXT_RECEIVE, MBN_SMS_CAPS_TEXT_SEND, mbn.mbn_sms_caps, mbnapi/MBN_SMS_CAPS, mbnapi/MBN_SMS_CAPS_NONE, mbnapi/MBN_SMS_CAPS_PDU_RECEIVE, mbnapi/MBN_SMS_CAPS_PDU_SEND, mbnapi/MBN_SMS_CAPS_TEXT_RECEIVE, mbnapi/MBN_SMS_CAPS_TEXT_SEND
f1_keywords:
- mbnapi/MBN_SMS_CAPS
dev_langs:
- c++
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
targetos: Windows
req.typenames: MBN_SMS_CAPS
req.redist: 
ms.custom: 19H1
---

# MBN_SMS_CAPS enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_SMS_CAPS</b> enumerated type contains bitfield values that specify  SMS capabilities.

These enumerated values are used by the <b>smsCaps</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/ns-mbnapi-mbn_interface_caps">MBN_INTERFACE_CAPS</a> structure.


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

