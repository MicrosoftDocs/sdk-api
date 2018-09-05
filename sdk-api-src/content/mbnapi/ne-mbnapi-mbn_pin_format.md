---
UID: NE:mbnapi.MBN_PIN_FORMAT
title: MBN_PIN_FORMAT
author: windows-sdk-content
description: The MBN_PIN_FORMAT enumerated type indicates whether a PIN is numeric or alphanumeric.
old-location: mbn\mbn_pin_format.htm
old-project: mbn
ms.assetid: a383f152-b5c2-46db-a3e8-977e9cd0caa4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: MBN_PIN_FORMAT, MBN_PIN_FORMAT enumeration [Microsoft Broadband Networks], MBN_PIN_FORMAT_ALPHANUMERIC, MBN_PIN_FORMAT_NONE, MBN_PIN_FORMAT_NUMERIC, mbn.mbn_pin_format, mbnapi/MBN_PIN_FORMAT, mbnapi/MBN_PIN_FORMAT_ALPHANUMERIC, mbnapi/MBN_PIN_FORMAT_NONE, mbnapi/MBN_PIN_FORMAT_NUMERIC
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mbnapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MBN_PIN_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mbnapi.h
api_name:
 - MBN_PIN_FORMAT
product: Windows
targetos: Windows
req.lib: 
req.dll: Mapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# MBN_PIN_FORMAT enumeration


## -description


The <b>MBN_PIN_FORMAT</b> enumerated type indicates whether a PIN is numeric or alphanumeric.


## -enum-fields




### -field MBN_PIN_FORMAT_NONE

Indicates that the PIN format is not known.


### -field MBN_PIN_FORMAT_NUMERIC

Indicates that the PIN is in numeric format.  The only allowed characters are 0-9.


### -field MBN_PIN_FORMAT_ALPHANUMERIC

Indicates that the PIN is in alphanumeric format.  Allowed characters are a-z, A-Z, 0-9, *, and #.

