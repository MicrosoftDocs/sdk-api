---
UID: NE:mbnapi.MBN_CELLULAR_CLASS
title: MBN_CELLULAR_CLASS (mbnapi.h)
description: The MBN_CELLULAR_CLASS enumerated type defines the type of cellular device.
helpviewer_keywords: ["MBN_CELLULAR_CLASS","MBN_CELLULAR_CLASS enumeration [Microsoft Broadband Networks]","MBN_CELLULAR_CLASS_CDMA","MBN_CELLULAR_CLASS_GSM","MBN_CELLULAR_CLASS_NONE","mbn.mbn_cellular_class","mbnapi/MBN_CELLULAR_CLASS","mbnapi/MBN_CELLULAR_CLASS_CDMA","mbnapi/MBN_CELLULAR_CLASS_GSM","mbnapi/MBN_CELLULAR_CLASS_NONE"]
old-location: mbn\mbn_cellular_class.htm
tech.root: mbn
ms.assetid: 2d75c20b-1ae4-4824-8918-41c20327a007
ms.date: 12/05/2018
ms.keywords: MBN_CELLULAR_CLASS, MBN_CELLULAR_CLASS enumeration [Microsoft Broadband Networks], MBN_CELLULAR_CLASS_CDMA, MBN_CELLULAR_CLASS_GSM, MBN_CELLULAR_CLASS_NONE, mbn.mbn_cellular_class, mbnapi/MBN_CELLULAR_CLASS, mbnapi/MBN_CELLULAR_CLASS_CDMA, mbnapi/MBN_CELLULAR_CLASS_GSM, mbnapi/MBN_CELLULAR_CLASS_NONE
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
req.typenames: MBN_CELLULAR_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_CELLULAR_CLASS
 - mbnapi/MBN_CELLULAR_CLASS
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
 - MBN_CELLULAR_CLASS
---

# MBN_CELLULAR_CLASS enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_CELLULAR_CLASS</b> enumerated type defines the type of cellular device.

## -enum-fields

### -field MBN_CELLULAR_CLASS_NONE:0

No cellular class.

### -field MBN_CELLULAR_CLASS_GSM:0x1

GSM cellular class.

### -field MBN_CELLULAR_CLASS_CDMA:0x2

CDMA cellular class.

