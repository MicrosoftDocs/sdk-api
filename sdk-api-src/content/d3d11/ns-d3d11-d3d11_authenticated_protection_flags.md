---
UID: NS:d3d11.D3D11_AUTHENTICATED_PROTECTION_FLAGS
title: D3D11_AUTHENTICATED_PROTECTION_FLAGS
author: windows-driver-content
description: Specifies the protection level for video content.
old-location: mf\d3d11_authenticated_protection_flags.htm
old-project: medfound
ms.assetid: 037AB541-2E68-460C-8626-7F22C6C3E425
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: D3D11_AUTHENTICATED_PROTECTION_FLAGS, D3D11_AUTHENTICATED_PROTECTION_FLAGS union [Media Foundation], d3d11/D3D11_AUTHENTICATED_PROTECTION_FLAGS, mf.d3d11_authenticated_protection_flags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_AUTHENTICATED_PROTECTION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d11.h
api_name:
-	D3D11_AUTHENTICATED_PROTECTION_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_AUTHENTICATED_PROTECTION_FLAGS structure


## -description


Specifies the protection level for video content.


## -struct-fields




### -field Flags


### -field Flags.ProtectionEnabled

If 1, video content protection is enabled.




### -field Flags.OverlayOrFullscreenRequired

If 1, the application requires video to be displayed using either a hardware overlay or full-screen exclusive mode.


### -field Flags.Reserved

Reserved. Set all bits to zero.




### -field __MIDL___MIDL_itf_d3d11_0000_0034_0001

 


### -field Value

Use this member to access all of the bits in the union.




## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>
 

 

