---
UID: NE:dxgi1_2.DXGI_ALPHA_MODE
title: DXGI_ALPHA_MODE
author: windows-sdk-content
description: Identifies the alpha value, transparency behavior, of a surface.
old-location: direct3ddxgi\dxgi_alpha_mode.htm
tech.root: direct3ddxgi
ms.assetid: DD3D1E49-06D2-4FB9-A41B-86453D8E566F
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DXGI_ALPHA_MODE, DXGI_ALPHA_MODE enumeration [DXGI], DXGI_ALPHA_MODE_FORCE_DWORD, DXGI_ALPHA_MODE_IGNORE, DXGI_ALPHA_MODE_PREMULTIPLIED, DXGI_ALPHA_MODE_STRAIGHT, DXGI_ALPHA_MODE_UNSPECIFIED, direct3ddxgi.dxgi_alpha_mode, dxgi1_2/DXGI_ALPHA_MODE, dxgi1_2/DXGI_ALPHA_MODE_FORCE_DWORD, dxgi1_2/DXGI_ALPHA_MODE_IGNORE, dxgi1_2/DXGI_ALPHA_MODE_PREMULTIPLIED, dxgi1_2/DXGI_ALPHA_MODE_STRAIGHT, dxgi1_2/DXGI_ALPHA_MODE_UNSPECIFIED
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: dxgi1_2.h
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
 - DXGI1_2.h
api_name:
 - DXGI_ALPHA_MODE
product: Windows
targetos: Windows
req.typenames: DXGI_ALPHA_MODE
req.redist: 
---

# DXGI_ALPHA_MODE enumeration


## -description


Identifies the alpha value, transparency behavior, of a surface.


## -enum-fields




### -field DXGI_ALPHA_MODE_UNSPECIFIED

Indicates that the transparency behavior is not specified.


### -field DXGI_ALPHA_MODE_PREMULTIPLIED

Indicates that the transparency behavior is premultiplied. Each color is first scaled by the alpha value. The alpha value itself is the same in both straight and premultiplied alpha. Typically, no color channel value is greater than the alpha channel value. If a color channel value in a premultiplied format is greater than the alpha channel, the standard source-over blending math results in an additive blend.


### -field DXGI_ALPHA_MODE_STRAIGHT

Indicates that the transparency behavior is not premultiplied. The alpha channel indicates the transparency of the color.


### -field DXGI_ALPHA_MODE_IGNORE

Indicates to ignore the transparency behavior.


### -field DXGI_ALPHA_MODE_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile 
          to a size other than 32 bits. This value is not used.


## -remarks



For more information about alpha mode, see <a href="https://msdn.microsoft.com/f1b1e735-2e89-4dc1-9fee-dfb4626ef453">D2D1_ALPHA_MODE</a>.




## -see-also




<a href="https://msdn.microsoft.com/c4574c89-dee2-4841-9318-5383cf417111">DXGI Enumerations</a>



<a href="https://msdn.microsoft.com/38B302DF-5617-4195-8E4A-619D75188AD5">DXGI_SWAP_CHAIN_DESC1</a>
 

 

