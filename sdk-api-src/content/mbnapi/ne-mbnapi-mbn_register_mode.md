---
UID: NE:mbnapi.MBN_REGISTER_MODE
title: MBN_REGISTER_MODE (mbnapi.h)
description: The MBN_REGISTER_MODE enumerated type indicates the network selection mode of a device.
helpviewer_keywords: ["MBN_REGISTER_MODE","MBN_REGISTER_MODE enumeration [Microsoft Broadband Networks]","MBN_REGISTER_MODE_AUTOMATIC","MBN_REGISTER_MODE_MANUAL","MBN_REGISTER_MODE_NONE","mbn.mbn_register_mode","mbnapi/MBN_REGISTER_MODE","mbnapi/MBN_REGISTER_MODE_AUTOMATIC","mbnapi/MBN_REGISTER_MODE_MANUAL","mbnapi/MBN_REGISTER_MODE_NONE"]
old-location: mbn\mbn_register_mode.htm
tech.root: mbn
ms.assetid: be64aa55-5a31-4909-9f34-634f7b14fc30
ms.date: 12/05/2018
ms.keywords: MBN_REGISTER_MODE, MBN_REGISTER_MODE enumeration [Microsoft Broadband Networks], MBN_REGISTER_MODE_AUTOMATIC, MBN_REGISTER_MODE_MANUAL, MBN_REGISTER_MODE_NONE, mbn.mbn_register_mode, mbnapi/MBN_REGISTER_MODE, mbnapi/MBN_REGISTER_MODE_AUTOMATIC, mbnapi/MBN_REGISTER_MODE_MANUAL, mbnapi/MBN_REGISTER_MODE_NONE
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
req.typenames: MBN_REGISTER_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_REGISTER_MODE
 - mbnapi/MBN_REGISTER_MODE
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
 - MBN_REGISTER_MODE
---

# MBN_REGISTER_MODE enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_REGISTER_MODE</b> enumerated type indicates the network selection mode of a device.

## -enum-fields

### -field MBN_REGISTER_MODE_NONE:0

No network selection mode is defined.

### -field MBN_REGISTER_MODE_AUTOMATIC

The device automatically selects the network to which to register .

### -field MBN_REGISTER_MODE_MANUAL

The device tries to register to a given network.

