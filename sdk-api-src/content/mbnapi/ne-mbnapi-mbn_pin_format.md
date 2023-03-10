---
UID: NE:mbnapi.MBN_PIN_FORMAT
title: MBN_PIN_FORMAT (mbnapi.h)
description: The MBN_PIN_FORMAT enumerated type indicates whether a PIN is numeric or alphanumeric.
helpviewer_keywords: ["MBN_PIN_FORMAT","MBN_PIN_FORMAT enumeration [Microsoft Broadband Networks]","MBN_PIN_FORMAT_ALPHANUMERIC","MBN_PIN_FORMAT_NONE","MBN_PIN_FORMAT_NUMERIC","mbn.mbn_pin_format","mbnapi/MBN_PIN_FORMAT","mbnapi/MBN_PIN_FORMAT_ALPHANUMERIC","mbnapi/MBN_PIN_FORMAT_NONE","mbnapi/MBN_PIN_FORMAT_NUMERIC"]
old-location: mbn\mbn_pin_format.htm
tech.root: mbn
ms.assetid: a383f152-b5c2-46db-a3e8-977e9cd0caa4
ms.date: 12/05/2018
ms.keywords: MBN_PIN_FORMAT, MBN_PIN_FORMAT enumeration [Microsoft Broadband Networks], MBN_PIN_FORMAT_ALPHANUMERIC, MBN_PIN_FORMAT_NONE, MBN_PIN_FORMAT_NUMERIC, mbn.mbn_pin_format, mbnapi/MBN_PIN_FORMAT, mbnapi/MBN_PIN_FORMAT_ALPHANUMERIC, mbnapi/MBN_PIN_FORMAT_NONE, mbnapi/MBN_PIN_FORMAT_NUMERIC
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
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
req.typenames: MBN_PIN_FORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_PIN_FORMAT
 - mbnapi/MBN_PIN_FORMAT
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
 - MBN_PIN_FORMAT
---

# MBN_PIN_FORMAT enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_PIN_FORMAT</b> enumerated type indicates whether a PIN is numeric or alphanumeric.

## -enum-fields

### -field MBN_PIN_FORMAT_NONE:0

Indicates that the PIN format is not known.

### -field MBN_PIN_FORMAT_NUMERIC

Indicates that the PIN is in numeric format.  The only allowed characters are 0-9.

### -field MBN_PIN_FORMAT_ALPHANUMERIC

Indicates that the PIN is in alphanumeric format.  Allowed characters are a-z, A-Z, 0-9, *, and #.

