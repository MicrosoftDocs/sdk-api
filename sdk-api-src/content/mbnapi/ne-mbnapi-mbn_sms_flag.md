---
UID: NE:mbnapi.MBN_SMS_FLAG
title: MBN_SMS_FLAG
author: windows-sdk-content
description: The MBN_SMS_FLAG enumerated type specifies the SMS message class.
old-location: mbn\mbn_sms_flag.htm
old-project: mbn
ms.assetid: caabe2b2-86f0-40e7-b5ee-aeda8b64651a
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: MBN_SMS_FLAG, MBN_SMS_FLAG enumeration [Microsoft Broadband Networks], MBN_SMS_FLAG_ALL, MBN_SMS_FLAG_DRAFT, MBN_SMS_FLAG_INDEX, MBN_SMS_FLAG_NEW, MBN_SMS_FLAG_OLD, MBN_SMS_FLAG_SENT, mbn.mbn_sms_flag, mbnapi/MBN_SMS_FLAG, mbnapi/MBN_SMS_FLAG_ALL, mbnapi/MBN_SMS_FLAG_DRAFT, mbnapi/MBN_SMS_FLAG_INDEX, mbnapi/MBN_SMS_FLAG_NEW, mbnapi/MBN_SMS_FLAG_OLD, mbnapi/MBN_SMS_FLAG_SENT
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MBN_SMS_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mbnapi.h
api_name:
 - MBN_SMS_FLAG
product: Windows
targetos: Windows
req.lib: 
req.dll: Mapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# MBN_SMS_FLAG enumeration


## -description


The <b>MBN_SMS_FLAG</b> enumerated type specifies the SMS message class.

These enumerated values are used in the <a href="https://msdn.microsoft.com/f8dffd7b-3c12-43da-b61c-3c9aa8f1136f">MBN_SMS_FILTER</a> structure.


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

