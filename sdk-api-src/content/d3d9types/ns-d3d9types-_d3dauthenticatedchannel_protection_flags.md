---
UID: NS:d3d9types._D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS
title: "_D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS"
author: windows-driver-content
description: Specifies the protection level for video content.
old-location: mf\d3dauthenticatedchannel_protection_flags.htm
old-project: medfound
ms.assetid: 681c6ad9-cf55-47e4-bbb9-e7fdc499a709
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS, D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS structure [Media Foundation], _D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS, d3d9types/D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS, mf.d3dauthenticatedchannel_protection_flags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d9types.h
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
req.typenames: D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS structure


## -description


Specifies the protection level for video content.


## -struct-fields




### -field ProtectionEnabled

If 1, video content protection is enabled.


### -field OverlayOrFullscreenRequired

If 1, the application requires video to be displayed using either a hardware overlay or full-screen exclusive mode.


### -field Reserved

Reserved. Set all bits to zero.


#### - Value

Use this member to access all of the bits in the union.


## -see-also




<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>
 

 

