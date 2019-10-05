---
UID: NE:mfidl.MFTOPOLOGY_HARDWARE_MODE
title: MFTOPOLOGY_HARDWARE_MODE (mfidl.h)
author: windows-sdk-content
description: Specifies whether the topology loader will insert hardware-based Media Foundation transforms (MFTs) into the topology.
old-location: mf\mftopology_hardware_mode.htm
tech.root: medfound
ms.assetid: fdaa13a5-9b23-440e-be04-ae926e1b0ff5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MFTOPOLOGY_HARDWARE_MODE, MFTOPOLOGY_HARDWARE_MODE enumeration [Media Foundation], MFTOPOLOGY_HWMODE_SOFTWARE_ONLY, MFTOPOLOGY_HWMODE_USE_HARDWARE, MFTOPOLOGY_HWMODE_USE_ONLY_HARDWARE, mf.mftopology_hardware_mode, mfidl/ MFTOPOLOGY_HWMODE_USE_ONLY_HARDWARE, mfidl/MFTOPOLOGY_HARDWARE_MODE, mfidl/MFTOPOLOGY_HWMODE_SOFTWARE_ONLY, mfidl/MFTOPOLOGY_HWMODE_USE_HARDWARE
ms.topic: enum
f1_keywords: 
 - "mfidl/MFTOPOLOGY_HARDWARE_MODE"
dev_langs:
 - c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFTOPOLOGY_HARDWARE_MODE
targetos: Windows
req.typenames: MFTOPOLOGY_HARDWARE_MODE
req.redist: 
ms.custom: 19H1
---

# MFTOPOLOGY_HARDWARE_MODE enumeration


## -description


Specifies whether the topology loader will insert hardware-based Media Foundation transforms (MFTs) into the topology.


## -enum-fields




### -field MFTOPOLOGY_HWMODE_SOFTWARE_ONLY

Use only software  MFTs. Do not use hardware-based MFTs. This mode is the default, for backward compatibility with existing applications.


### -field MFTOPOLOGY_HWMODE_USE_HARDWARE

Use hardware-based MFTs when possible, and software MFTs otherwise. This mode is the recommended one.


### -field MFTOPOLOGY_HWMODE_USE_ONLY_HARDWARE

If hardware-based MFTs are available, the topoloader will insert
    them.  If not, the connection will fail.

Supported in Windows 8.1 and later.


## -remarks



This enumeration is used with the <a href="https://docs.microsoft.com/windows/desktop/medfound/mf-topology-hardware-mode">MF_TOPOLOGY_HARDWARE_MODE</a> topology attribute.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
 

 

