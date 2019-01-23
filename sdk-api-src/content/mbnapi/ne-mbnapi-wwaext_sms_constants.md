---
UID: NE:mbnapi.MBN_SMS_CONSTANTS
title: WWAEXT_SMS_CONSTANTS
author: windows-sdk-content
description: The MBN_SMS_CONSTANTS enumerated type contains SMS constant values.
old-location: mbn\mbn_sms_constants.htm
tech.root: mbn
ms.assetid: 2d81e9f7-5e1d-4291-84ad-56578d2f4ae4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MBN_CDMA_SHORT_MSG_SIZE_MAX, MBN_CDMA_SHORT_MSG_SIZE_UNKNOWN, MBN_MESSAGE_INDEX_NONE, MBN_SMS_CONSTANTS, MBN_SMS_CONSTANTS enumeration [Microsoft Broadband Networks], WWAEXT_SMS_CONSTANTS, WWAEXT_SMS_CONSTANTS enumeration [Microsoft Broadband Networks], mbn.mbn_sms_constants, mbnapi/MBN_CDMA_SHORT_MSG_SIZE_MAX, mbnapi/MBN_CDMA_SHORT_MSG_SIZE_UNKNOWN, mbnapi/MBN_MESSAGE_INDEX_NONE, mbnapi/MBN_SMS_CONSTANTS
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
 - WWAEXT_SMS_CONSTANTS
product: Windows
targetos: Windows
req.typenames: WWAEXT_SMS_CONSTANTS
req.redist: 
---

# WWAEXT_SMS_CONSTANTS enumeration


## -description


The <b>MBN_SMS_CONSTANTS</b> enumerated type contains SMS constant values.


## -enum-fields




### -field MBN_MESSAGE_INDEX_NONE

The message is not stored in device memory.  This constant is used by <a href="https://msdn.microsoft.com/dc0e15c4-6203-4105-9d19-5931b27047d2">IMbnSmsReadMsgPdu</a> and <a href="https://msdn.microsoft.com/d26b09f7-eb83-46ed-82cb-a702d3af5d05">IMbnSmsReadMsgTextCdma</a>.


### -field MBN_CDMA_SHORT_MSG_SIZE_UNKNOWN

The device does not support SMS.  This constant is used by <a href="https://msdn.microsoft.com/ee261c32-aa17-496a-a568-d9da43e1e23a">IMbnSmsConfiguration</a>.


### -field MBN_CDMA_SHORT_MSG_SIZE_MAX

The maximum size of a CDMA short message.  

