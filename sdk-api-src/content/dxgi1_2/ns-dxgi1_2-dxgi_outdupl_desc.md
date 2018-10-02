---
UID: NS:dxgi1_2.DXGI_OUTDUPL_DESC
title: DXGI_OUTDUPL_DESC
author: windows-sdk-content
description: The DXGI_OUTDUPL_DESC structure describes the dimension of the output and the surface that contains the desktop image. The format of the desktop image is always DXGI_FORMAT_B8G8R8A8_UNORM.
old-location: direct3ddxgi\dxgi_outdupl_desc.htm
tech.root: direct3ddxgi
ms.assetid: 003014E3-4322-4253-8D69-AE315CDFDA75
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DXGI_OUTDUPL_DESC, DXGI_OUTDUPL_DESC structure [DXGI], direct3ddxgi.dxgi_outdupl_desc, dxgi1_2/DXGI_OUTDUPL_DESC
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps only]
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
 - DXGI_OUTDUPL_DESC
product: Windows
targetos: Windows
req.typenames: DXGI_OUTDUPL_DESC
req.redist: 
---

# DXGI_OUTDUPL_DESC structure


## -description


The DXGI_OUTDUPL_DESC structure describes the dimension of the output and the surface that contains the desktop image. The format of the desktop image is always <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT_B8G8R8A8_UNORM</a>.


## -struct-fields




### -field ModeDesc

A <a href="https://msdn.microsoft.com/en-us/library/Bb173064(v=VS.85).aspx">DXGI_MODE_DESC</a> structure that describes the display mode of the duplicated output.


### -field Rotation

A member of the <a href="https://msdn.microsoft.com/en-us/library/Bb173065(v=VS.85).aspx">DXGI_MODE_ROTATION</a> enumerated type that describes how the duplicated output rotates an image.


### -field DesktopImageInSystemMemory

Specifies whether the resource that contains the desktop image is already located in system memory. <b>TRUE</b> if the resource is in system memory; otherwise, <b>FALSE</b>. If this value is <b>TRUE</b> and  the application requires CPU access, it can use the <a href="https://msdn.microsoft.com/1FFFF954-0AD2-418E-B0CC-D674994C3CCE">IDXGIOutputDuplication::MapDesktopSurface</a> and <a href="https://msdn.microsoft.com/1B9AF088-5856-4F1C-A794-6CF870D62A29">IDXGIOutputDuplication::UnMapDesktopSurface</a> methods to avoid copying the data into a staging buffer.


## -remarks



This structure is used by <a href="https://msdn.microsoft.com/40D2CF38-1528-48A4-BC0C-5D8CC132D0CB">GetDesc</a>.




## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>
 

 

