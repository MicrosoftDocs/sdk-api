---
UID: NS:d3d11.D3D11_FEATURE_DATA_D3D9_OPTIONS
title: D3D11_FEATURE_DATA_D3D9_OPTIONS
author: windows-sdk-content
description: Describes Direct3D 9 feature options in the current graphics driver.
old-location: direct3d11\d3d11_feature_data_d3d9_options.htm
tech.root: direct3d11
ms.assetid: E5262261-28D7-4F7A-AB9A-A73FEADAE8FD
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: D3D11_FEATURE_DATA_D3D9_OPTIONS, D3D11_FEATURE_DATA_D3D9_OPTIONS structure [Direct3D 11], d3d11/D3D11_FEATURE_DATA_D3D9_OPTIONS, direct3d11.d3d11_feature_data_d3d9_options
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - D3D11.h
api_name:
 - D3D11_FEATURE_DATA_D3D9_OPTIONS
product: Windows
targetos: Windows
req.typenames: D3D11_FEATURE_DATA_D3D9_OPTIONS
req.redist: 
---

# D3D11_FEATURE_DATA_D3D9_OPTIONS structure


## -description


<div class="alert"><b>Note</b>  This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</div><div> </div>Describes Direct3D 9 feature options in the current graphics driver.


## -struct-fields




### -field FullNonPow2TextureSupport

Specifies whether the driver supports the nonpowers-of-2-unconditionally feature. For more information about this feature, see <a href="https://msdn.microsoft.com/en-us/library/Ff476876(v=VS.85).aspx">feature level</a>. The runtime sets this member to <b>TRUE</b> for hardware at Direct3D 10 and higher feature levels.  For hardware at Direct3D 9.3 and lower feature levels, the runtime sets this member to <b>FALSE</b> if the hardware and driver support the powers-of-2 (2D textures must have widths and heights specified as powers of two) feature or the nonpowers-of-2-conditionally feature. For more information about this feature, see feature level.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476155(v=VS.85).aspx">Core Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476124(v=VS.85).aspx">D3D11_FEATURE</a>
 

 

