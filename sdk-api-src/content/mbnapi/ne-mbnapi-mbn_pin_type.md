---
UID: NE:mbnapi.MBN_PIN_TYPE
title: MBN_PIN_TYPE (mbnapi.h)
description: The MBN_PIN_TYPE enumerated type indicates the type of password required for unlocking the information stored on the interface.
helpviewer_keywords: ["MBN_PIN_TYPE","MBN_PIN_TYPE enumeration [Microsoft Broadband Networks]","MBN_PIN_TYPE_CORPORATE_PIN","MBN_PIN_TYPE_CUSTOM","MBN_PIN_TYPE_DEVICE_FIRST_SIM_PIN","MBN_PIN_TYPE_DEVICE_SIM_PIN","MBN_PIN_TYPE_NETWORK_PIN","MBN_PIN_TYPE_NETWORK_SUBSET_PIN","MBN_PIN_TYPE_NONE","MBN_PIN_TYPE_PIN1","MBN_PIN_TYPE_PIN2","MBN_PIN_TYPE_SUBSIDY_LOCK","MBN_PIN_TYPE_SVC_PROVIDER_PIN","mbn.mbn_pin_type","mbnapi/MBN_PIN_TYPE","mbnapi/MBN_PIN_TYPE_CORPORATE_PIN","mbnapi/MBN_PIN_TYPE_CUSTOM","mbnapi/MBN_PIN_TYPE_DEVICE_FIRST_SIM_PIN","mbnapi/MBN_PIN_TYPE_DEVICE_SIM_PIN","mbnapi/MBN_PIN_TYPE_NETWORK_PIN","mbnapi/MBN_PIN_TYPE_NETWORK_SUBSET_PIN","mbnapi/MBN_PIN_TYPE_NONE","mbnapi/MBN_PIN_TYPE_PIN1","mbnapi/MBN_PIN_TYPE_PIN2","mbnapi/MBN_PIN_TYPE_SUBSIDY_LOCK","mbnapi/MBN_PIN_TYPE_SVC_PROVIDER_PIN"]
old-location: mbn\mbn_pin_type.htm
tech.root: mbn
ms.assetid: 79791522-cf6b-4dae-a9c2-68e9e2fc394f
ms.date: 12/05/2018
ms.keywords: MBN_PIN_TYPE, MBN_PIN_TYPE enumeration [Microsoft Broadband Networks], MBN_PIN_TYPE_CORPORATE_PIN, MBN_PIN_TYPE_CUSTOM, MBN_PIN_TYPE_DEVICE_FIRST_SIM_PIN, MBN_PIN_TYPE_DEVICE_SIM_PIN, MBN_PIN_TYPE_NETWORK_PIN, MBN_PIN_TYPE_NETWORK_SUBSET_PIN, MBN_PIN_TYPE_NONE, MBN_PIN_TYPE_PIN1, MBN_PIN_TYPE_PIN2, MBN_PIN_TYPE_SUBSIDY_LOCK, MBN_PIN_TYPE_SVC_PROVIDER_PIN, mbn.mbn_pin_type, mbnapi/MBN_PIN_TYPE, mbnapi/MBN_PIN_TYPE_CORPORATE_PIN, mbnapi/MBN_PIN_TYPE_CUSTOM, mbnapi/MBN_PIN_TYPE_DEVICE_FIRST_SIM_PIN, mbnapi/MBN_PIN_TYPE_DEVICE_SIM_PIN, mbnapi/MBN_PIN_TYPE_NETWORK_PIN, mbnapi/MBN_PIN_TYPE_NETWORK_SUBSET_PIN, mbnapi/MBN_PIN_TYPE_NONE, mbnapi/MBN_PIN_TYPE_PIN1, mbnapi/MBN_PIN_TYPE_PIN2, mbnapi/MBN_PIN_TYPE_SUBSIDY_LOCK, mbnapi/MBN_PIN_TYPE_SVC_PROVIDER_PIN
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
req.typenames: MBN_PIN_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_PIN_TYPE
 - mbnapi/MBN_PIN_TYPE
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
 - MBN_PIN_TYPE
---

# MBN_PIN_TYPE enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_PIN_TYPE</b> enumerated type indicates the type of password required for unlocking the information stored on the interface.

## -enum-fields

### -field MBN_PIN_TYPE_NONE:0

Indicates that no PIN is pending to be entered.

### -field MBN_PIN_TYPE_CUSTOM

Indicates a custom PIN code.

### -field MBN_PIN_TYPE_PIN1

Indicates a PIN1 code.  For CDMA devices, PIN1 represents the power-on device lock code.  For GSM devices, PIN1 represents the SIM lock, also referred to  as PIN in GSM terminology.

### -field MBN_PIN_TYPE_PIN2

Indicates a PIN2 code.

### -field MBN_PIN_TYPE_DEVICE_SIM_PIN

Indicates a device to SIM password.

### -field MBN_PIN_TYPE_DEVICE_FIRST_SIM_PIN

Indicates a device to very first SIM password.

### -field MBN_PIN_TYPE_NETWORK_PIN

Indicates a network personalization password.

### -field MBN_PIN_TYPE_NETWORK_SUBSET_PIN

Indicates a network subset personalization password.

### -field MBN_PIN_TYPE_SVC_PROVIDER_PIN

Indicates a Service Provider (SP) personalization password.

### -field MBN_PIN_TYPE_CORPORATE_PIN

Indicates a corporate personalization password.

### -field MBN_PIN_TYPE_SUBSIDY_LOCK

Indicates a subsidy unlock code.

