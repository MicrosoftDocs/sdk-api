---
UID: NE:mbnapi.MBN_INTERFACE_CAPS_CONSTANTS
title: MBN_INTERFACE_CAPS_CONSTANTS (mbnapi.h)
description: The MBN_INTERFACE_CAPS_CONSTANTS enumerated type defines the maximum length of string values used by assorted elements of the MBN_INTERFACE_CAPS structure.
helpviewer_keywords: ["MBN_DEVICEID_LEN","MBN_FIRMWARE_LEN","MBN_INTERFACE_CAPS_CONSTANTS","MBN_INTERFACE_CAPS_CONSTANTS enumeration [Microsoft Broadband Networks]","MBN_MANUFACTURER_LEN","MBN_MODEL_LEN","mbn.mbn_interface_caps_constants","mbnapi/MBN_DEVICEID_LEN","mbnapi/MBN_FIRMWARE_LEN","mbnapi/MBN_INTERFACE_CAPS_CONSTANTS","mbnapi/MBN_MANUFACTURER_LEN","mbnapi/MBN_MODEL_LEN"]
old-location: mbn\mbn_interface_caps_constants.htm
tech.root: mbn
ms.assetid: d5478721-7d7b-487e-b223-0240f3451aed
ms.date: 12/05/2018
ms.keywords: MBN_DEVICEID_LEN, MBN_FIRMWARE_LEN, MBN_INTERFACE_CAPS_CONSTANTS, MBN_INTERFACE_CAPS_CONSTANTS enumeration [Microsoft Broadband Networks], MBN_MANUFACTURER_LEN, MBN_MODEL_LEN, mbn.mbn_interface_caps_constants, mbnapi/MBN_DEVICEID_LEN, mbnapi/MBN_FIRMWARE_LEN, mbnapi/MBN_INTERFACE_CAPS_CONSTANTS, mbnapi/MBN_MANUFACTURER_LEN, mbnapi/MBN_MODEL_LEN
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
req.typenames: MBN_INTERFACE_CAPS_CONSTANTS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_INTERFACE_CAPS_CONSTANTS
 - mbnapi/MBN_INTERFACE_CAPS_CONSTANTS
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
 - MBN_INTERFACE_CAPS_CONSTANTS
---

# MBN_INTERFACE_CAPS_CONSTANTS enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_INTERFACE_CAPS_CONSTANTS</b> enumerated type defines the maximum length of string values used by assorted elements of the <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_interface_caps">MBN_INTERFACE_CAPS</a> structure.

## -enum-fields

### -field MBN_DEVICEID_LEN:18

This constant defines the maximum string size of the <b>deviceID</b> member of the <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_interface_caps">MBN_INTERFACE_CAPS</a> structure.

### -field MBN_MANUFACTURER_LEN:32

This constant defines the maximum string size of the <b>manufacturer</b> member of the <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_interface_caps">MBN_INTERFACE_CAPS</a> structure.

### -field MBN_MODEL_LEN:32

This constant defines the maximum string size of the <b>model</b> member of the <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_interface_caps">MBN_INTERFACE_CAPS</a> structure.

### -field MBN_FIRMWARE_LEN:32

This constant defines the maximum string size of the <b>firmwareInfo</b> member of the <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_interface_caps">MBN_INTERFACE_CAPS</a> structure.
