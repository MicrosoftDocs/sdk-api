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

# D3D12_STREAM_OUTPUT_DESC structure


## -description


Describes a streaming output buffer.


## -struct-fields




### -field pSODeclaration


            An array of <a href="https://msdn.microsoft.com/F16FA746-2213-4F11-85AD-2CDCB0744618">D3D12_SO_DECLARATION_ENTRY</a> structures. Can't be <b>NULL</b> if <b>NumEntries</b> &gt; 0.
          


### -field NumEntries


            The number of entries in the stream output declaration array that the <b>pSODeclaration</b> member points to.
          


### -field pBufferStrides


            An array of buffer strides; each stride is the size of an element for that buffer.
          


### -field NumStrides


            The number of strides (or buffers) that the <b>pBufferStrides</b> member points to.
          


### -field RasterizedStream


            The index number of the stream to be sent to the rasterizer stage.
          


## -remarks




        A <a href="https://msdn.microsoft.com/35D10150-A633-4D38-B684-3E2DF357FFC0">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a> object contains a <b>D3D12_STREAM_OUTPUT_DESC</b> structure.
      




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

