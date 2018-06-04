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

# ID3D12GraphicsCommandList::SOSetTargets


## -description



          Sets the stream output buffer views.
        


## -parameters




### -param StartSlot [in]

Type: <b>UINT</b>


            Index into the device's zero-based array to begin setting stream output buffers.

          


### -param NumViews [in]

Type: <b>UINT</b>


            The number of entries in the <i>pViews</i> array.
          


### -param pViews [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/EFA4FBD7-3063-4B6A-B3B1-45418C6682FC">D3D12_STREAM_OUTPUT_BUFFER_VIEW</a>*</b>


            Specifies an array of  <a href="https://msdn.microsoft.com/EFA4FBD7-3063-4B6A-B3B1-45418C6682FC">D3D12_STREAM_OUTPUT_BUFFER_VIEW</a> structures.
          


## -returns




            This method does not return a value.
          




## -see-also




<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>
 

 

