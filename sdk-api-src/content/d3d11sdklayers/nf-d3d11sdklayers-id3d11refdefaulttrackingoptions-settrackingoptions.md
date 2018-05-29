---
UID: NF:d3d11sdklayers.ID3D11RefDefaultTrackingOptions.SetTrackingOptions
title: ID3D11RefDefaultTrackingOptions::SetTrackingOptions
author: windows-sdk-content
description: Sets graphics processing unit (GPU) debug reference default tracking options for specific resource types.
old-location: direct3d11\id3d11refdefaulttrackingoptions_settrackingoptions.htm
old-project: direct3d11
ms.assetid: A54AAC4C-CD38-4326-AF99-9FB74CC0A1A0
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: ID3D11RefDefaultTrackingOptions interface [Direct3D 11],SetTrackingOptions method, ID3D11RefDefaultTrackingOptions.SetTrackingOptions, ID3D11RefDefaultTrackingOptions::SetTrackingOptions, SetTrackingOptions, SetTrackingOptions method [Direct3D 11], SetTrackingOptions method [Direct3D 11],ID3D11RefDefaultTrackingOptions interface, d3d11sdklayers/ID3D11RefDefaultTrackingOptions::SetTrackingOptions, direct3d11.id3d11refdefaulttrackingoptions_settrackingoptions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11sdklayers.h
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
req.typenames: D3D11_SHADER_TRACKING_RESOURCE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3DCompiler.lib
-	D3DCompiler.dll
api_name:
-	ID3D11RefDefaultTrackingOptions.SetTrackingOptions
product: Windows
targetos: Windows
req.lib: D3DCompiler.lib
req.dll: 
req.irql: 
---

# ID3D11RefDefaultTrackingOptions::SetTrackingOptions


## -description



        Sets graphics processing unit (GPU) debug reference default tracking options for specific resource types.
      


## -parameters




### -param ResourceTypeFlags


            A <a href="https://msdn.microsoft.com/148303AC-E373-4D41-BDF5-0E17B2A3D366">D3D11_SHADER_TRACKING_RESOURCE_TYPE</a>-typed value that specifies the type of resource to track.
          


### -param Options

A combination of <a href="https://msdn.microsoft.com/20C152CD-B155-4B46-8F41-EDDEC60494DF">D3D11_SHADER_TRACKING_OPTIONS</a>-typed flags that are combined by using a bitwise <b>OR</b> operation. The resulting value identifies tracking options. If a flag is present, the tracking option that the flag represents is set to "on"; otherwise the tracking option is set to "off."


## -returns




            This method returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 return codes</a>.
          




## -remarks




        This API requires the Windows Software Development Kit (SDK) for Windows 8.
      




## -see-also




<a href="https://msdn.microsoft.com/B6DD9810-275E-466B-8FE8-64EED0933B45">ID3D11RefDefaultTrackingOptions</a>
 

 

