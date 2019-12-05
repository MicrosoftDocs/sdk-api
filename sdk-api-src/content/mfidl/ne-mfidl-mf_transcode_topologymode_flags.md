---
UID: NE:mfidl._MF_TRANSCODE_TOPOLOGYMODE_FLAGS
title: MF_TRANSCODE_TOPOLOGYMODE_FLAGS (mfidl.h)
description: Defines flags for the MF_TRANSCODE_TOPOLOGYMODE attribute.
old-location: mf\mf_transcode_topologymode_flags.htm
tech.root: medfound
ms.assetid: 9a98a052-9fb0-4c63-bc9c-8e112e37973f
ms.date: 12/05/2018
ms.keywords: MF_TRANSCODE_TOPOLOGYMODE_FLAGS, MF_TRANSCODE_TOPOLOGYMODE_FLAGS enumeration [Media Foundation], MF_TRANSCODE_TOPOLOGYMODE_HARDWARE_ALLOWED, MF_TRANSCODE_TOPOLOGYMODE_SOFTWARE_ONLY, mf.mf_transcode_topologymode_flags, mfidl/MF_TRANSCODE_TOPOLOGYMODE_FLAGS, mfidl/MF_TRANSCODE_TOPOLOGYMODE_HARDWARE_ALLOWED, mfidl/MF_TRANSCODE_TOPOLOGYMODE_SOFTWARE_ONLY
ms.topic: enum
f1_keywords:
- mfidl/MF_TRANSCODE_TOPOLOGYMODE_FLAGS
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
- MF_TRANSCODE_TOPOLOGYMODE_FLAGS
targetos: Windows
req.typenames: MF_TRANSCODE_TOPOLOGYMODE_FLAGS
req.redist: 
ms.custom: 19H1
---

# MF_TRANSCODE_TOPOLOGYMODE_FLAGS enumeration


## -description


Defines flags for the <a href="https://docs.microsoft.com/windows/desktop/medfound/mf-transcode-topologymode">MF_TRANSCODE_TOPOLOGYMODE</a> attribute.


## -enum-fields




### -field MF_TRANSCODE_TOPOLOGYMODE_SOFTWARE_ONLY

The topology loader will exclude hardware-based transforms (such as codecs and color converters) from the topology. It will use only software transforms.


### -field MF_TRANSCODE_TOPOLOGYMODE_HARDWARE_ALLOWED

The topology loader may insert hardware-based transforms into the transcode topology.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
 

 

