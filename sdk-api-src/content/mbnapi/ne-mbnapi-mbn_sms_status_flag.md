---
UID: NE:mbnapi.MBN_SMS_STATUS_FLAG
title: MBN_SMS_STATUS_FLAG (mbnapi.h)
description: The MBN_SMS_STATUS_FLAG enumerated type indicates the status of a device's SMS message store.
helpviewer_keywords: ["MBN_SMS_FLAG_MESSAGE_STORE_FULL","MBN_SMS_FLAG_NEW_MESSAGE","MBN_SMS_FLAG_NONE","MBN_SMS_STATUS_FLAG","MBN_SMS_STATUS_FLAG enumeration [Microsoft Broadband Networks]","mbn.mbn_sms_status_flag","mbnapi/MBN_SMS_FLAG_MESSAGE_STORE_FULL","mbnapi/MBN_SMS_FLAG_NEW_MESSAGE","mbnapi/MBN_SMS_FLAG_NONE","mbnapi/MBN_SMS_STATUS_FLAG"]
old-location: mbn\mbn_sms_status_flag.htm
tech.root: mbn
ms.assetid: 835cfdfa-face-4779-8bbf-e35076b85521
ms.date: 12/05/2018
ms.keywords: MBN_SMS_FLAG_MESSAGE_STORE_FULL, MBN_SMS_FLAG_NEW_MESSAGE, MBN_SMS_FLAG_NONE, MBN_SMS_STATUS_FLAG, MBN_SMS_STATUS_FLAG enumeration [Microsoft Broadband Networks], mbn.mbn_sms_status_flag, mbnapi/MBN_SMS_FLAG_MESSAGE_STORE_FULL, mbnapi/MBN_SMS_FLAG_NEW_MESSAGE, mbnapi/MBN_SMS_FLAG_NONE, mbnapi/MBN_SMS_STATUS_FLAG
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
req.typenames: MBN_SMS_STATUS_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_SMS_STATUS_FLAG
 - mbnapi/MBN_SMS_STATUS_FLAG
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
 - MBN_SMS_STATUS_FLAG
---

# MBN_SMS_STATUS_FLAG enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_SMS_STATUS_FLAG</b> enumerated type indicates the status of  a device's SMS message store.

These enumerated values are used in a bitfield by the <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_sms_status_info">MBN_SMS_STATUS_INFO</a> structure.

## -enum-fields

### -field MBN_SMS_FLAG_NONE:0

There is no SMS status information to report.

### -field MBN_SMS_FLAG_MESSAGE_STORE_FULL:0x1

The message store is full.

### -field MBN_SMS_FLAG_NEW_MESSAGE:0x2

A new non-class 0 message has been received by the interface.
