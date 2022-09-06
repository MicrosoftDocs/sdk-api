---
UID: NE:mbnapi.MBN_SMS_CONSTANTS
title: WWAEXT_SMS_CONSTANTS (mbnapi.h)
description: The MBN_SMS_CONSTANTS enumerated type contains SMS constant values.
helpviewer_keywords: ["MBN_CDMA_SHORT_MSG_SIZE_MAX","MBN_CDMA_SHORT_MSG_SIZE_UNKNOWN","MBN_MESSAGE_INDEX_NONE","MBN_SMS_CONSTANTS","MBN_SMS_CONSTANTS enumeration [Microsoft Broadband Networks]","WWAEXT_SMS_CONSTANTS","WWAEXT_SMS_CONSTANTS enumeration [Microsoft Broadband Networks]","mbn.mbn_sms_constants","mbnapi/MBN_CDMA_SHORT_MSG_SIZE_MAX","mbnapi/MBN_CDMA_SHORT_MSG_SIZE_UNKNOWN","mbnapi/MBN_MESSAGE_INDEX_NONE","mbnapi/MBN_SMS_CONSTANTS"]
old-location: mbn\mbn_sms_constants.htm
tech.root: mbn
ms.assetid: 2d81e9f7-5e1d-4291-84ad-56578d2f4ae4
ms.date: 12/05/2018
ms.keywords: MBN_CDMA_SHORT_MSG_SIZE_MAX, MBN_CDMA_SHORT_MSG_SIZE_UNKNOWN, MBN_MESSAGE_INDEX_NONE, MBN_SMS_CONSTANTS, MBN_SMS_CONSTANTS enumeration [Microsoft Broadband Networks], WWAEXT_SMS_CONSTANTS, WWAEXT_SMS_CONSTANTS enumeration [Microsoft Broadband Networks], mbn.mbn_sms_constants, mbnapi/MBN_CDMA_SHORT_MSG_SIZE_MAX, mbnapi/MBN_CDMA_SHORT_MSG_SIZE_UNKNOWN, mbnapi/MBN_MESSAGE_INDEX_NONE, mbnapi/MBN_SMS_CONSTANTS
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
req.typenames: WWAEXT_SMS_CONSTANTS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_SMS_CONSTANTS
 - mbnapi/MBN_SMS_CONSTANTS
 - WWAEXT_SMS_CONSTANTS
 - mbnapi/WWAEXT_SMS_CONSTANTS
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
 - WWAEXT_SMS_CONSTANTS
---

# WWAEXT_SMS_CONSTANTS enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_SMS_CONSTANTS</b> enumerated type contains SMS constant values.

## -enum-fields

### -field MBN_MESSAGE_INDEX_NONE:0

The message is not stored in device memory.  This constant is used by <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsreadmsgpdu">IMbnSmsReadMsgPdu</a> and <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsreadmsgtextcdma">IMbnSmsReadMsgTextCdma</a>.

### -field MBN_CDMA_SHORT_MSG_SIZE_UNKNOWN:0

The device does not support SMS.  This constant is used by <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsconfiguration">IMbnSmsConfiguration</a>.

### -field MBN_CDMA_SHORT_MSG_SIZE_MAX:160

The maximum size of a CDMA short message.
