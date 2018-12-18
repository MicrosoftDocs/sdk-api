---
UID: NS:mbnapi.MBN_SMS_FILTER
title: MBN_SMS_FILTER
author: windows-sdk-content
description: The MBN_SMS_FILTER structure contains the values that describe a set of SMS messages.
old-location: mbn\mbn_sms_filter.htm
tech.root: mbn
ms.assetid: f8dffd7b-3c12-43da-b61c-3c9aa8f1136f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MBN_SMS_FILTER, MBN_SMS_FILTER structure [Microsoft Broadband Networks], mbn.mbn_sms_filter, mbnapi/MBN_SMS_FILTER
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
 - MBN_SMS_FILTER
product: Windows
targetos: Windows
req.typenames: MBN_SMS_FILTER
req.redist: 
---

# MBN_SMS_FILTER structure


## -description


The <b>MBN_SMS_FILTER</b> structure contains the values that describe a set of SMS messages.


## -struct-fields




### -field flag

An <a href="https://msdn.microsoft.com/caabe2b2-86f0-40e7-b5ee-aeda8b64651a">MBN_SMS_FLAG</a> value that 	specifies the message class.


### -field messageIndex

Contains the index of a particular message in device memory.  This value is only meaningful when <b>flag</b> is set to 	<b>MBN_SMS_FLAG_INDEX</b>.  The maximum range of this value is from 1 to the <a href="https://msdn.microsoft.com/c7dee4b7-4a34-4d08-aae3-7455531a9556">MaxMessageIndex</a> property of <a href="https://msdn.microsoft.com/ee261c32-aa17-496a-a568-d9da43e1e23a">IMbnSmsConfiguration</a>. 

