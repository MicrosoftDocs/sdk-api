---
UID: NE:mbnapi.MBN_SMS_CDMA_ENCODING
title: MBN_SMS_CDMA_ENCODING (mbnapi.h)
description: The MBN_SMS_CDMA_ENCODING enumerated type specifies character encoding types for CDMA.
helpviewer_keywords: ["MBN_SMS_CDMA_ENCODING","MBN_SMS_CDMA_ENCODING enumeration [Microsoft Broadband Networks]","MBN_SMS_CDMA_ENCODING_7BIT_ASCII","MBN_SMS_CDMA_ENCODING_EPM","MBN_SMS_CDMA_ENCODING_GSM_7BIT","MBN_SMS_CDMA_ENCODING_IA5","MBN_SMS_CDMA_ENCODING_KOREAN","MBN_SMS_CDMA_ENCODING_LATIN","MBN_SMS_CDMA_ENCODING_LATIN_HEBREW","MBN_SMS_CDMA_ENCODING_OCTET","MBN_SMS_CDMA_ENCODING_SHIFT_JIS","MBN_SMS_CDMA_ENCODING_UNICODE","mbn.mbn_sms_cdma_encoding","mbnapi/MBN_SMS_CDMA_ENCODING","mbnapi/MBN_SMS_CDMA_ENCODING_7BIT_ASCII","mbnapi/MBN_SMS_CDMA_ENCODING_EPM","mbnapi/MBN_SMS_CDMA_ENCODING_GSM_7BIT","mbnapi/MBN_SMS_CDMA_ENCODING_IA5","mbnapi/MBN_SMS_CDMA_ENCODING_KOREAN","mbnapi/MBN_SMS_CDMA_ENCODING_LATIN","mbnapi/MBN_SMS_CDMA_ENCODING_LATIN_HEBREW","mbnapi/MBN_SMS_CDMA_ENCODING_OCTET","mbnapi/MBN_SMS_CDMA_ENCODING_SHIFT_JIS","mbnapi/MBN_SMS_CDMA_ENCODING_UNICODE"]
old-location: mbn\mbn_sms_cdma_encoding.htm
tech.root: mbn
ms.assetid: c556d615-de98-4d05-86e4-88df84e98258
ms.date: 12/05/2018
ms.keywords: MBN_SMS_CDMA_ENCODING, MBN_SMS_CDMA_ENCODING enumeration [Microsoft Broadband Networks], MBN_SMS_CDMA_ENCODING_7BIT_ASCII, MBN_SMS_CDMA_ENCODING_EPM, MBN_SMS_CDMA_ENCODING_GSM_7BIT, MBN_SMS_CDMA_ENCODING_IA5, MBN_SMS_CDMA_ENCODING_KOREAN, MBN_SMS_CDMA_ENCODING_LATIN, MBN_SMS_CDMA_ENCODING_LATIN_HEBREW, MBN_SMS_CDMA_ENCODING_OCTET, MBN_SMS_CDMA_ENCODING_SHIFT_JIS, MBN_SMS_CDMA_ENCODING_UNICODE, mbn.mbn_sms_cdma_encoding, mbnapi/MBN_SMS_CDMA_ENCODING, mbnapi/MBN_SMS_CDMA_ENCODING_7BIT_ASCII, mbnapi/MBN_SMS_CDMA_ENCODING_EPM, mbnapi/MBN_SMS_CDMA_ENCODING_GSM_7BIT, mbnapi/MBN_SMS_CDMA_ENCODING_IA5, mbnapi/MBN_SMS_CDMA_ENCODING_KOREAN, mbnapi/MBN_SMS_CDMA_ENCODING_LATIN, mbnapi/MBN_SMS_CDMA_ENCODING_LATIN_HEBREW, mbnapi/MBN_SMS_CDMA_ENCODING_OCTET, mbnapi/MBN_SMS_CDMA_ENCODING_SHIFT_JIS, mbnapi/MBN_SMS_CDMA_ENCODING_UNICODE
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
req.typenames: MBN_SMS_CDMA_ENCODING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_SMS_CDMA_ENCODING
 - mbnapi/MBN_SMS_CDMA_ENCODING
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
 - MBN_SMS_CDMA_ENCODING
---

# MBN_SMS_CDMA_ENCODING enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_SMS_CDMA_ENCODING</b> enumerated type specifies character encoding types for CDMA.

## -enum-fields

### -field MBN_SMS_CDMA_ENCODING_OCTET:0

Octet encoding.

### -field MBN_SMS_CDMA_ENCODING_EPM

EPM encoding.

### -field MBN_SMS_CDMA_ENCODING_7BIT_ASCII

7 bit ASCII encoding.

### -field MBN_SMS_CDMA_ENCODING_IA5

IA5 encoding.

### -field MBN_SMS_CDMA_ENCODING_UNICODE

Unicode encoding.

### -field MBN_SMS_CDMA_ENCODING_SHIFT_JIS

Shift JIS encoding for the Japanese Language.

### -field MBN_SMS_CDMA_ENCODING_KOREAN

Korean encoding.

### -field MBN_SMS_CDMA_ENCODING_LATIN_HEBREW

Latin Hebrew encoding.

### -field MBN_SMS_CDMA_ENCODING_LATIN

Latin encoding.

### -field MBN_SMS_CDMA_ENCODING_GSM_7BIT

GSM 7 bit encoding.

## -remarks

The encodings are defined in section 4.5.2 of the 3GPP2 specification C.S0015-B "Short Message Service (SM) for Wideband Spread Spectrum Systems".

