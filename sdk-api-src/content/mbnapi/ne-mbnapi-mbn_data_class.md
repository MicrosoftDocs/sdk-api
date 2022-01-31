---
UID: NE:mbnapi.MBN_DATA_CLASS
title: MBN_DATA_CLASS (mbnapi.h)
description: The MBN_DATA_CLASS enumerated type specifies the data classes that a provider supports.
helpviewer_keywords: ["MBN_DATA_CLASS","MBN_DATA_CLASS enumeration [Microsoft Broadband Networks]","MBN_DATA_CLASS_1XEVDO","MBN_DATA_CLASS_1XEVDO_REVA","MBN_DATA_CLASS_1XEVDO_REVB","MBN_DATA_CLASS_1XEVDV","MBN_DATA_CLASS_1XRTT","MBN_DATA_CLASS_3XRTT","MBN_DATA_CLASS_CUSTOM","MBN_DATA_CLASS_EDGE","MBN_DATA_CLASS_GPRS","MBN_DATA_CLASS_HSDPA","MBN_DATA_CLASS_HSUPA","MBN_DATA_CLASS_LTE","MBN_DATA_CLASS_NONE","MBN_DATA_CLASS_UMB","MBN_DATA_CLASS_UMTS","mbn.mbn_data_class","mbnapi/MBN_DATA_CLASS","mbnapi/MBN_DATA_CLASS_1XEVDO","mbnapi/MBN_DATA_CLASS_1XEVDO_REVA","mbnapi/MBN_DATA_CLASS_1XEVDO_REVB","mbnapi/MBN_DATA_CLASS_1XEVDV","mbnapi/MBN_DATA_CLASS_1XRTT","mbnapi/MBN_DATA_CLASS_3XRTT","mbnapi/MBN_DATA_CLASS_CUSTOM","mbnapi/MBN_DATA_CLASS_EDGE","mbnapi/MBN_DATA_CLASS_GPRS","mbnapi/MBN_DATA_CLASS_HSDPA","mbnapi/MBN_DATA_CLASS_HSUPA","mbnapi/MBN_DATA_CLASS_LTE","mbnapi/MBN_DATA_CLASS_NONE","mbnapi/MBN_DATA_CLASS_UMB","mbnapi/MBN_DATA_CLASS_UMTS"]
old-location: mbn\mbn_data_class.htm
tech.root: mbn
ms.assetid: 798d5d72-9267-433f-b890-9302a0a600f2
ms.date: 12/05/2018
ms.keywords: MBN_DATA_CLASS, MBN_DATA_CLASS enumeration [Microsoft Broadband Networks], MBN_DATA_CLASS_1XEVDO, MBN_DATA_CLASS_1XEVDO_REVA, MBN_DATA_CLASS_1XEVDO_REVB, MBN_DATA_CLASS_1XEVDV, MBN_DATA_CLASS_1XRTT, MBN_DATA_CLASS_3XRTT, MBN_DATA_CLASS_CUSTOM, MBN_DATA_CLASS_EDGE, MBN_DATA_CLASS_GPRS, MBN_DATA_CLASS_HSDPA, MBN_DATA_CLASS_HSUPA, MBN_DATA_CLASS_LTE, MBN_DATA_CLASS_NONE, MBN_DATA_CLASS_UMB, MBN_DATA_CLASS_UMTS, mbn.mbn_data_class, mbnapi/MBN_DATA_CLASS, mbnapi/MBN_DATA_CLASS_1XEVDO, mbnapi/MBN_DATA_CLASS_1XEVDO_REVA, mbnapi/MBN_DATA_CLASS_1XEVDO_REVB, mbnapi/MBN_DATA_CLASS_1XEVDV, mbnapi/MBN_DATA_CLASS_1XRTT, mbnapi/MBN_DATA_CLASS_3XRTT, mbnapi/MBN_DATA_CLASS_CUSTOM, mbnapi/MBN_DATA_CLASS_EDGE, mbnapi/MBN_DATA_CLASS_GPRS, mbnapi/MBN_DATA_CLASS_HSDPA, mbnapi/MBN_DATA_CLASS_HSUPA, mbnapi/MBN_DATA_CLASS_LTE, mbnapi/MBN_DATA_CLASS_NONE, mbnapi/MBN_DATA_CLASS_UMB, mbnapi/MBN_DATA_CLASS_UMTS
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
req.typenames: MBN_DATA_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_DATA_CLASS
 - mbnapi/MBN_DATA_CLASS
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
 - MBN_DATA_CLASS
---

# MBN_DATA_CLASS enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_DATA_CLASS</b> enumerated type specifies the data classes that a provider supports.

## -enum-fields

### -field MBN_DATA_CLASS_NONE:0

No data class.

### -field MBN_DATA_CLASS_GPRS:0x1

The GPRS data class implemented by GSM providers.

### -field MBN_DATA_CLASS_EDGE:0x2

 The EDGE data class implemented by GSM providers.

### -field MBN_DATA_CLASS_UMTS:0x4

The UMTS data class implemented by mobile radio providers.

### -field MBN_DATA_CLASS_HSDPA:0x8

The HSDPA data class implemented by mobile radio providers.

### -field MBN_DATA_CLASS_HSUPA:0x10

The HSUPA (High Speed Uplink Packet Access) data class.

### -field MBN_DATA_CLASS_LTE:0x20

The LTE data class implemented by mobile radio providers.

### -field MBN_DATA_CLASS_1XRTT:0x10000

The 1xRTT data class implemented by CDMA providers.

### -field MBN_DATA_CLASS_1XEVDO:0x20000

The IxEV-DO data class implemented by CDMA providers.

### -field MBN_DATA_CLASS_1XEVDO_REVA:0x40000

The IxEV-DO RevA data class implemented by CDMA providers.

### -field MBN_DATA_CLASS_1XEVDV:0x80000

The 1xXEV-DV data class.

### -field MBN_DATA_CLASS_3XRTT:0x100000

The 3xRTT data class.

### -field MBN_DATA_CLASS_1XEVDO_REVB:0x200000

 The 1xEV-DO RevB data class, which is defined for future use.

### -field MBN_DATA_CLASS_UMB:0x400000

 The UMB data class.

### -field MBN_DATA_CLASS_CUSTOM:0x80000000

 The custom data class.

