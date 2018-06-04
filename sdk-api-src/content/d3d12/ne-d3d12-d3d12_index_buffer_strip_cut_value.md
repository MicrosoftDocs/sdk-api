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

# D3D12_INDEX_BUFFER_STRIP_CUT_VALUE enumeration


## -description



                  When using triangle strip primitive topology, vertex positions are interpreted as vertices of a continuous triangle “strip”.  There is a special index value that represents the desire to have a discontinuity in the strip, the cut index value. This enum lists the supported cut values.



## -enum-fields




### -field D3D12_INDEX_BUFFER_STRIP_CUT_VALUE_DISABLED


            Indicates that there is no cut value.
          


### -field D3D12_INDEX_BUFFER_STRIP_CUT_VALUE_0xFFFF


            Indicates that 0xFFFF should be used as the cut value.
          


### -field D3D12_INDEX_BUFFER_STRIP_CUT_VALUE_0xFFFFFFFF


            Indicates that 0xFFFFFFFF should be used as the cut value.
          


## -remarks




          This enum is used by the <a href="https://msdn.microsoft.com/35D10150-A633-4D38-B684-3E2DF357FFC0">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a> structure.
        




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

