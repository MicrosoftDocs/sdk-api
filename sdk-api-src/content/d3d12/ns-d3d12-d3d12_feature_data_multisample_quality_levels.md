---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS structure


## -description



          Describes the image quality levels for a given format and sample count.
        


## -struct-fields




### -field Format


            A <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a>-typed value for the format to return info about.
          


### -field SampleCount


            The number of multi-samples per pixel to return info about.
          


### -field Flags


            Flags to control quality levels, as a bitwise-OR'd combination of <a href="https://msdn.microsoft.com/78FBD851-879C-4C84-ACEA-58CF4ADE29A0">D3D12_MULTISAMPLE_QUALITY_LEVEL_FLAGS</a> enumeration constants.
            The resulting value specifies options for determining quality levels.
          


### -field NumQualityLevels


            The number of quality levels.
          


## -remarks




        See <a href="https://msdn.microsoft.com/165ECFE0-1B18-4A26-8B9C-3CE53776A349">D3D12_FEATURE</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/165ECFE0-1B18-4A26-8B9C-3CE53776A349">D3D12_FEATURE</a>
 

 

