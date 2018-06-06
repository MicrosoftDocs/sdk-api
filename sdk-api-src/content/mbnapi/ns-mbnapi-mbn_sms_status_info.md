---
UID: NS:mbnapi.MBN_SMS_STATUS_INFO
title: MBN_SMS_STATUS_INFO
author: windows-sdk-content
description: The MBN_SMS_STATUS_INFO structure contains the status of the SMS message store of a device.
old-location: mbn\mbn_sms_status_info.htm
old-project: mbn
ms.assetid: 9146d230-c96c-4d70-9bc5-e91896e19d35
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: MBN_SMS_STATUS_INFO, MBN_SMS_STATUS_INFO structure [Microsoft Broadband Networks], mbn.mbn_sms_status_info, mbnapi/MBN_SMS_STATUS_INFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: MBN_SMS_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mbnapi.h
api_name:
 - MBN_SMS_STATUS_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MBN_SMS_STATUS_INFO structure


## -description


The <b>MBN_SMS_STATUS_INFO</b> structure contains the status of the SMS message store of a device.


## -struct-fields




### -field flag

A bitwise OR combination of <a href="https://msdn.microsoft.com/835cfdfa-face-4779-8bbf-e35076b85521">MBN_SMS_STATUS_FLAG</a> values that specify the state of the message store.


### -field messageIndex

Contains the index of the last received message in the store.  This field is only meaningful when <b>flag</b> contains <b>MBN_SMS_FLAG_NEW_MESSAGE</b>.

