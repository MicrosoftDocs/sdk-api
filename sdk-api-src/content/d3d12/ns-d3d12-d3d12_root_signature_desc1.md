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

# D3D12_ROOT_SIGNATURE_DESC1 structure


## -description


Describes the layout of a root signature version 1.1.


## -struct-fields




### -field NumParameters


            The number of slots in the root signature. This number is also the number of elements in the <i>pParameters</i> array.
          


### -field pParameters


            An array of <a href="https://msdn.microsoft.com/615B8ABF-FD80-4254-976B-9E587CE9F12E">D3D12_ROOT_PARAMETER1</a> structures for the slots in the root signature.
          


### -field NumStaticSamplers

Specifies the number of static samplers.


### -field pStaticSamplers


            Pointer to one or more <a href="https://msdn.microsoft.com/35553C1C-3661-4778-8BC5-F2E6775DF96D">D3D12_STATIC_SAMPLER_DESC</a> structures.
          


### -field Flags

Specifies the <a href="https://msdn.microsoft.com/C3118E58-2006-459F-B2D6-4EC84F2BC058">D3D12_ROOT_SIGNATURE_FLAGS</a> that determine the data volatility.


## -remarks



Use this structure with the <a href="https://msdn.microsoft.com/46F692DD-55FF-4DFF-AF11-78CAD10922C1">D3D12_VERSIONED_ROOT_SIGNATURE_DESC</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/D74D9D3B-96AB-489A-A91C-4F68AC3D05EE">D3D12_ROOT_SIGNATURE_DESC</a>



<a href="https://msdn.microsoft.com/8FE42C1C-7F1D-4E70-A7EE-D5EC67237327">Root Signature Version 1.1</a>
 

 

