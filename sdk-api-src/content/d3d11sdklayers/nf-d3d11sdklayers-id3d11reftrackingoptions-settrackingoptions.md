---
UID: NF:d3d11sdklayers.ID3D11RefTrackingOptions.SetTrackingOptions
title: ID3D11RefTrackingOptions::SetTrackingOptions
author: windows-sdk-content
description: Sets graphics processing unit (GPU) debug reference tracking options.
old-location: direct3d11\id3d11reftrackingoptions_settrackingoptions.htm
tech.root: direct3d11
ms.assetid: 2C782DBE-BA76-4D2E-82D6-1A03941B2FB1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ID3D11RefTrackingOptions interface [Direct3D 11],SetTrackingOptions method, ID3D11RefTrackingOptions.SetTrackingOptions, ID3D11RefTrackingOptions::SetTrackingOptions, SetTrackingOptions, SetTrackingOptions method [Direct3D 11], SetTrackingOptions method [Direct3D 11],ID3D11RefTrackingOptions interface, d3d11sdklayers/ID3D11RefTrackingOptions::SetTrackingOptions, direct3d11.id3d11reftrackingoptions_settrackingoptions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11sdklayers.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3DCompiler.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler.lib
 - D3DCompiler.dll
api_name:
 - ID3D11RefTrackingOptions.SetTrackingOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11RefTrackingOptions::SetTrackingOptions


## -description


Sets graphics processing unit (GPU) debug reference tracking options.


## -parameters




### -param uOptions

A combination of <a href="https://msdn.microsoft.com/en-us/library/Hh404501(v=VS.85).aspx">D3D11_SHADER_TRACKING_OPTIONS</a>-typed flags that are combined by using a bitwise <b>OR</b> operation. The resulting value identifies tracking options. If a flag is present, the tracking option that the flag represents is set to "on"; otherwise the tracking option is set to "off."


## -returns



This method returns one of the <a href="https://msdn.microsoft.com/en-us/library/Ff476174(v=VS.85).aspx">Direct3D 11 return codes</a>.




## -remarks



This API requires the Windows Software Development Kit (SDK) for Windows 8.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh446836(v=VS.85).aspx">ID3D11RefTrackingOptions</a>
 

 

