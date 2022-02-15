---
UID: NE:mbnapi.MBN_SMS_FORMAT
title: MBN_SMS_FORMAT (mbnapi.h)
description: Format of SMS messages.
helpviewer_keywords: ["MBN_SMS_FORMAT","MBN_SMS_FORMAT enumeration [Microsoft Broadband Networks]","MBN_SMS_FORMAT_NONE","MBN_SMS_FORMAT_PDU","MBN_SMS_FORMAT_TEXT","mbn.mbn_sms_format","mbnapi/MBN_SMS_FORMAT","mbnapi/MBN_SMS_FORMAT_NONE","mbnapi/MBN_SMS_FORMAT_PDU","mbnapi/MBN_SMS_FORMAT_TEXT"]
old-location: mbn\mbn_sms_format.htm
tech.root: mbn
ms.assetid: ece079e2-43a2-4ca9-9aa7-1b9484f0176e
ms.date: 12/05/2018
ms.keywords: MBN_SMS_FORMAT, MBN_SMS_FORMAT enumeration [Microsoft Broadband Networks], MBN_SMS_FORMAT_NONE, MBN_SMS_FORMAT_PDU, MBN_SMS_FORMAT_TEXT, mbn.mbn_sms_format, mbnapi/MBN_SMS_FORMAT, mbnapi/MBN_SMS_FORMAT_NONE, mbnapi/MBN_SMS_FORMAT_PDU, mbnapi/MBN_SMS_FORMAT_TEXT
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
targetos: Windows
req.typenames: MBN_SMS_FORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_SMS_FORMAT
 - mbnapi/MBN_SMS_FORMAT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mbnapi.h
api_name:
 - MBN_SMS_FORMAT
---

# MBN_SMS_FORMAT enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_SMS_FORMAT</b> enumerated type specifies the format of SMS messages.

## -enum-fields

### -field MBN_SMS_FORMAT_NONE:0

No SMS format.

### -field MBN_SMS_FORMAT_PDU:0x1

For GSM devices, SMS, messages will be read in PDU format. 

For CDMA devices, SMS messages will be read in binary CDMA format.

### -field MBN_SMS_FORMAT_TEXT:0x2

For CDMA devices, SMS messages will be read in text format.

