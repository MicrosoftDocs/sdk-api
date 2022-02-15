---
UID: NE:mbnapi.MBN_VOICE_CLASS
title: MBN_VOICE_CLASS (mbnapi.h)
description: The MBN_VOICE_CLASS enumerated type specifies a device's voice capabilities and how they interact with the data service.
helpviewer_keywords: ["MBN_VOICE_CLASS","MBN_VOICE_CLASS enumeration [Microsoft Broadband Networks]","MBN_VOICE_CLASS_NONE","MBN_VOICE_CLASS_NO_VOICE","MBN_VOICE_CLASS_SEPARATE_VOICE_DATA","MBN_VOICE_CLASS_SIMULTANEOUS_VOICE_DATA","mbn.mbn_voice_class","mbnapi/MBN_VOICE_CLASS","mbnapi/MBN_VOICE_CLASS_NONE","mbnapi/MBN_VOICE_CLASS_NO_VOICE","mbnapi/MBN_VOICE_CLASS_SEPARATE_VOICE_DATA","mbnapi/MBN_VOICE_CLASS_SIMULTANEOUS_VOICE_DATA"]
old-location: mbn\mbn_voice_class.htm
tech.root: mbn
ms.assetid: d2654e97-4020-449f-9622-39392309d6f3
ms.date: 12/05/2018
ms.keywords: MBN_VOICE_CLASS, MBN_VOICE_CLASS enumeration [Microsoft Broadband Networks], MBN_VOICE_CLASS_NONE, MBN_VOICE_CLASS_NO_VOICE, MBN_VOICE_CLASS_SEPARATE_VOICE_DATA, MBN_VOICE_CLASS_SIMULTANEOUS_VOICE_DATA, mbn.mbn_voice_class, mbnapi/MBN_VOICE_CLASS, mbnapi/MBN_VOICE_CLASS_NONE, mbnapi/MBN_VOICE_CLASS_NO_VOICE, mbnapi/MBN_VOICE_CLASS_SEPARATE_VOICE_DATA, mbnapi/MBN_VOICE_CLASS_SIMULTANEOUS_VOICE_DATA
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
req.typenames: MBN_VOICE_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_VOICE_CLASS
 - mbnapi/MBN_VOICE_CLASS
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
 - MBN_VOICE_CLASS
---

# MBN_VOICE_CLASS enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

 The <b>MBN_VOICE_CLASS</b> enumerated type specifies a device's voice capabilities and how they interact with the data service.

## -enum-fields

### -field MBN_VOICE_CLASS_NONE:0

The device voice class is unknown.

### -field MBN_VOICE_CLASS_NO_VOICE:0x1

The device does not support voice calls.

### -field MBN_VOICE_CLASS_SEPARATE_VOICE_DATA:0x2

The device supports voice calls, but does not support simultaneous voice and data.

### -field MBN_VOICE_CLASS_SIMULTANEOUS_VOICE_DATA:0x3

The device supports simultaneous voice and data.

