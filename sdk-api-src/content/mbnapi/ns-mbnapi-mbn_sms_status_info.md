---
UID: NS:mbnapi.MBN_SMS_STATUS_INFO
title: MBN_SMS_STATUS_INFO (mbnapi.h)
description: The MBN_SMS_STATUS_INFO structure contains the status of the SMS message store of a device.
helpviewer_keywords: ["MBN_SMS_STATUS_INFO","MBN_SMS_STATUS_INFO structure [Microsoft Broadband Networks]","mbn.mbn_sms_status_info","mbnapi/MBN_SMS_STATUS_INFO"]
old-location: mbn\mbn_sms_status_info.htm
tech.root: mbn
ms.assetid: 9146d230-c96c-4d70-9bc5-e91896e19d35
ms.date: 12/05/2018
ms.keywords: MBN_SMS_STATUS_INFO, MBN_SMS_STATUS_INFO structure [Microsoft Broadband Networks], mbn.mbn_sms_status_info, mbnapi/MBN_SMS_STATUS_INFO
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
req.typenames: MBN_SMS_STATUS_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_SMS_STATUS_INFO
 - mbnapi/MBN_SMS_STATUS_INFO
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
 - MBN_SMS_STATUS_INFO
---

# MBN_SMS_STATUS_INFO structure


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_SMS_STATUS_INFO</b> structure contains the status of the SMS message store of a device.

## -struct-fields

### -field flag

A bitwise OR combination of <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_sms_status_flag">MBN_SMS_STATUS_FLAG</a> values that specify the state of the message store.

### -field messageIndex

Contains the index of the last received message in the store.  This field is only meaningful when <b>flag</b> contains <b>MBN_SMS_FLAG_NEW_MESSAGE</b>.