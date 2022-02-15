---
UID: NE:mbnapi.MBN_PIN_CONSTANTS
title: MBN_PIN_CONSTANTS (mbnapi.h)
description: The MBN_PIN_CONSTANTS enumerated type defines constant values used by the MBN_PIN_INFO structure.
helpviewer_keywords: ["MBN_ATTEMPTS_REMAINING_UNKNOWN","MBN_PIN_CONSTANTS","MBN_PIN_CONSTANTS enumeration [Microsoft Broadband Networks]","MBN_PIN_LENGTH_UNKNOWN","mbn.mbn_pin_constants","mbnapi/MBN_ATTEMPTS_REMAINING_UNKNOWN","mbnapi/MBN_PIN_CONSTANTS","mbnapi/MBN_PIN_LENGTH_UNKNOWN"]
old-location: mbn\mbn_pin_constants.htm
tech.root: mbn
ms.assetid: dff1b2d3-d5f7-4349-8602-f2b5ccff1f41
ms.date: 12/05/2018
ms.keywords: MBN_ATTEMPTS_REMAINING_UNKNOWN, MBN_PIN_CONSTANTS, MBN_PIN_CONSTANTS enumeration [Microsoft Broadband Networks], MBN_PIN_LENGTH_UNKNOWN, mbn.mbn_pin_constants, mbnapi/MBN_ATTEMPTS_REMAINING_UNKNOWN, mbnapi/MBN_PIN_CONSTANTS, mbnapi/MBN_PIN_LENGTH_UNKNOWN
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
req.typenames: MBN_PIN_CONSTANTS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_PIN_CONSTANTS
 - mbnapi/MBN_PIN_CONSTANTS
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
 - MBN_PIN_CONSTANTS
---

# MBN_PIN_CONSTANTS enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_PIN_CONSTANTS</b> enumerated type defines constant values used by the <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_pin_info">MBN_PIN_INFO</a> structure.

## -enum-fields

### -field MBN_ATTEMPTS_REMAINING_UNKNOWN:0xffffffff

Indicates that there is no available information available on the number of attempts remaining to enter a valid PIN.

### -field MBN_PIN_LENGTH_UNKNOWN:0xffffffff

Indicates that there is no available information on the length of the PIN.
