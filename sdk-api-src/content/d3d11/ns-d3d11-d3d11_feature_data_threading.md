---
UID: NS:d3d11.D3D11_FEATURE_DATA_THREADING
title: D3D11_FEATURE_DATA_THREADING
author: windows-sdk-content
description: Describes the multi-threading features that are supported by the current graphics driver.
old-location: direct3d11\d3d11_feature_data_threading.htm
tech.root: direct3d11
ms.assetid: 1ad7d4c4-9da2-42b0-a461-e514060e3005
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D11_FEATURE_DATA_THREADING, D3D11_FEATURE_DATA_THREADING structure [Direct3D 11], d3d11/D3D11_FEATURE_DATA_THREADING, direct3d11.d3d11_feature_data_threading, ef972430-170a-436c-cbf4-65409cc60040
ms.topic: struct
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - D3D11_FEATURE_DATA_THREADING
product: Windows
targetos: Windows
req.typenames: D3D11_FEATURE_DATA_THREADING
req.redist: 
---

# D3D11_FEATURE_DATA_THREADING structure


## -description


Describes the multi-threading features that are supported by the current graphics driver.


## -struct-fields




### -field DriverConcurrentCreates

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> means resources can be created concurrently on multiple threads while drawing; <b>FALSE</b> means that the presence of coarse synchronization will prevent concurrency.


### -field DriverCommandLists

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> means command lists are supported by the current driver; <b>FALSE</b> means that the API will emulate deferred contexts and command lists with software.


## -remarks



Use the D3D11_FEATURE_DATA_THREADING structure with the <a href="https://msdn.microsoft.com/7edf2ffd-908a-4cf8-9ac6-8fd14d7a0ea1">ID3D11Device::CheckFeatureSupport</a> method to determine multi-threading support.




## -see-also




<a href="https://msdn.microsoft.com/2a45182a-7114-4075-b8b8-147f52fe7aa9">Core Structures</a>
 

 

