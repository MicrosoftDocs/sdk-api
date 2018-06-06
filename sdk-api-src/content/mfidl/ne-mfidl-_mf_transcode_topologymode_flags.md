---
UID: NE:mfidl._MF_TRANSCODE_TOPOLOGYMODE_FLAGS
title: "_MF_TRANSCODE_TOPOLOGYMODE_FLAGS"
author: windows-sdk-content
description: Defines flags for the MF_TRANSCODE_TOPOLOGYMODE attribute.
old-location: mf\mf_transcode_topologymode_flags.htm
old-project: medfound
ms.assetid: 9a98a052-9fb0-4c63-bc9c-8e112e37973f
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: MF_TRANSCODE_TOPOLOGYMODE_FLAGS, MF_TRANSCODE_TOPOLOGYMODE_FLAGS enumeration [Media Foundation], MF_TRANSCODE_TOPOLOGYMODE_HARDWARE_ALLOWED, MF_TRANSCODE_TOPOLOGYMODE_SOFTWARE_ONLY, _MF_TRANSCODE_TOPOLOGYMODE_FLAGS, mf.mf_transcode_topologymode_flags, mfidl/MF_TRANSCODE_TOPOLOGYMODE_FLAGS, mfidl/MF_TRANSCODE_TOPOLOGYMODE_HARDWARE_ALLOWED, mfidl/MF_TRANSCODE_TOPOLOGYMODE_SOFTWARE_ONLY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: MF_TRANSCODE_TOPOLOGYMODE_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MF_TRANSCODE_TOPOLOGYMODE_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MF_TRANSCODE_TOPOLOGYMODE_FLAGS enumeration


## -description


Defines flags for the <a href="https://msdn.microsoft.com/33db8621-114a-4531-908f-f30034441973">MF_TRANSCODE_TOPOLOGYMODE</a> attribute.


## -enum-fields




### -field MF_TRANSCODE_TOPOLOGYMODE_SOFTWARE_ONLY

The topology loader will exclude hardware-based transforms (such as codecs and color converters) from the topology. It will use only software transforms.


### -field MF_TRANSCODE_TOPOLOGYMODE_HARDWARE_ALLOWED

The topology loader may insert hardware-based transforms into the transcode topology.


## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

