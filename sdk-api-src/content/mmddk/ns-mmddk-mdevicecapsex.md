---
UID: NS:mmddk.MDEVICECAPSEX
title: MDEVICECAPSEX (mmddk.h)
description: The MDEVICECAPSEX structure contains device capability information for Plug and Play (PnP) device drivers.
helpviewer_keywords: ["MDEVICECAPSEX","MDEVICECAPSEX structure [Audio Devices]","aud-prop_12e0eeb8-beac-4b01-8a5c-6e78f58f703b.xml","audio.mdevicecapsex","mmddk/MDEVICECAPSEX"]
old-location: audio\mdevicecapsex.htm
tech.root: audio
ms.assetid: d2da18d2-4ff3-47a8-9cd9-f8df03eed0a5
ms.date: 12/05/2018
ms.keywords: MDEVICECAPSEX, MDEVICECAPSEX structure [Audio Devices], aud-prop_12e0eeb8-beac-4b01-8a5c-6e78f58f703b.xml, audio.mdevicecapsex, mmddk/MDEVICECAPSEX
req.header: mmddk.h
req.include-header: Mmddk.h, Mmsystem.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows XP and later Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MDEVICECAPSEX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MDEVICECAPSEX
 - mmddk/MDEVICECAPSEX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mmddk.h
api_name:
 - MDEVICECAPSEX
---

# MDEVICECAPSEX structure


## -description

The <code>MDEVICECAPSEX</code> structure contains device capability information for Plug and Play (PnP) device drivers.

## -struct-fields

### -field cbSize

Specifies the size of the structure, in bytes.

### -field pCaps

Specifies the capabilities of the device. The format of this data is device specific.

