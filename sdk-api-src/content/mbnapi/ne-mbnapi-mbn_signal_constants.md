---
UID: NE:mbnapi.MBN_SIGNAL_CONSTANTS
title: MBN_SIGNAL_CONSTANTS (mbnapi.h)
description: THE MBN_SIGNAL_CONSTANTS enumerated type contains specific values used by IMbnSignal interface operations.
helpviewer_keywords: ["MBN_ERROR_RATE_UNKNOWN","MBN_RSSI_DEFAULT","MBN_RSSI_DISABLE","MBN_RSSI_UNKNOWN","MBN_SIGNAL_CONSTANTS","MBN_SIGNAL_CONSTANTS enumeration [Microsoft Broadband Networks]","mbn.mbn_signal_constants","mbnapi/MBN_ERROR_RATE_UNKNOWN","mbnapi/MBN_RSSI_DEFAULT","mbnapi/MBN_RSSI_DISABLE","mbnapi/MBN_RSSI_UNKNOWN","mbnapi/MBN_SIGNAL_CONSTANTS"]
old-location: mbn\mbn_signal_constants.htm
tech.root: mbn
ms.assetid: 0f790b85-5f01-41a8-940d-b4eda562bf75
ms.date: 12/05/2018
ms.keywords: MBN_ERROR_RATE_UNKNOWN, MBN_RSSI_DEFAULT, MBN_RSSI_DISABLE, MBN_RSSI_UNKNOWN, MBN_SIGNAL_CONSTANTS, MBN_SIGNAL_CONSTANTS enumeration [Microsoft Broadband Networks], mbn.mbn_signal_constants, mbnapi/MBN_ERROR_RATE_UNKNOWN, mbnapi/MBN_RSSI_DEFAULT, mbnapi/MBN_RSSI_DISABLE, mbnapi/MBN_RSSI_UNKNOWN, mbnapi/MBN_SIGNAL_CONSTANTS
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
req.typenames: MBN_SIGNAL_CONSTANTS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_SIGNAL_CONSTANTS
 - mbnapi/MBN_SIGNAL_CONSTANTS
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
 - MBN_SIGNAL_CONSTANTS
---

# MBN_SIGNAL_CONSTANTS enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

THE <b>MBN_SIGNAL_CONSTANTS</b> enumerated type contains specific values used by <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsignal">IMbnSignal</a> interface operations.

## -enum-fields

### -field MBN_RSSI_DEFAULT:0xffffffff

Use the default value for signal state reporting.

### -field MBN_RSSI_DISABLE:0

Disable signal state reporting.

### -field MBN_RSSI_UNKNOWN:99

Signal strength is unknown.

### -field MBN_ERROR_RATE_UNKNOWN:99

Signal error rate is unknown.
