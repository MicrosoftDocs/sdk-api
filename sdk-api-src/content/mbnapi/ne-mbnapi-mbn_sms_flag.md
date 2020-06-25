---
UID: NE:mbnapi.MBN_SMS_FLAG
title: MBN_SMS_FLAG (mbnapi.h)
description: The MBN_SMS_FLAG enumerated type specifies the SMS message class.
helpviewer_keywords: ["MBN_SMS_FLAG","MBN_SMS_FLAG enumeration [Microsoft Broadband Networks]","MBN_SMS_FLAG_ALL","MBN_SMS_FLAG_DRAFT","MBN_SMS_FLAG_INDEX","MBN_SMS_FLAG_NEW","MBN_SMS_FLAG_OLD","MBN_SMS_FLAG_SENT","mbn.mbn_sms_flag","mbnapi/MBN_SMS_FLAG","mbnapi/MBN_SMS_FLAG_ALL","mbnapi/MBN_SMS_FLAG_DRAFT","mbnapi/MBN_SMS_FLAG_INDEX","mbnapi/MBN_SMS_FLAG_NEW","mbnapi/MBN_SMS_FLAG_OLD","mbnapi/MBN_SMS_FLAG_SENT"]
old-location: mbn\mbn_sms_flag.htm
tech.root: mbn
ms.assetid: caabe2b2-86f0-40e7-b5ee-aeda8b64651a
ms.date: 12/05/2018
ms.keywords: MBN_SMS_FLAG, MBN_SMS_FLAG enumeration [Microsoft Broadband Networks], MBN_SMS_FLAG_ALL, MBN_SMS_FLAG_DRAFT, MBN_SMS_FLAG_INDEX, MBN_SMS_FLAG_NEW, MBN_SMS_FLAG_OLD, MBN_SMS_FLAG_SENT, mbn.mbn_sms_flag, mbnapi/MBN_SMS_FLAG, mbnapi/MBN_SMS_FLAG_ALL, mbnapi/MBN_SMS_FLAG_DRAFT, mbnapi/MBN_SMS_FLAG_INDEX, mbnapi/MBN_SMS_FLAG_NEW, mbnapi/MBN_SMS_FLAG_OLD, mbnapi/MBN_SMS_FLAG_SENT
f1_keywords:
- mbnapi/MBN_SMS_FLAG
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
- MBN_SMS_FLAG
targetos: Windows
req.typenames: MBN_SMS_FLAG
req.redist: 
ms.custom: 19H1
---

# MBN_SMS_FLAG enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_SMS_FLAG</b> enumerated type specifies the SMS message class.

These enumerated values are used in the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/ns-mbnapi-mbn_sms_filter">MBN_SMS_FILTER</a> structure.


## -enum-fields




### -field MBN_SMS_FLAG_ALL

Refers to all the messages in the device message store.


### -field MBN_SMS_FLAG_INDEX

Refers to a single message in the device message store.


### -field MBN_SMS_FLAG_NEW

Refers to all new received and unread messages.


### -field MBN_SMS_FLAG_OLD

Refers to all old and read messages.


### -field MBN_SMS_FLAG_SENT

Refers to all sent and saved messages.


### -field MBN_SMS_FLAG_DRAFT

Refers to all unsent and saved messages.

