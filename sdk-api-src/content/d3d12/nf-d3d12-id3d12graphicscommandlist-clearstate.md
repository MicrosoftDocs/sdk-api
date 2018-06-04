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

# ID3D12GraphicsCommandList::ClearState


## -description


Resets the state of a direct command list back to the state it was in when the command list was created.  


## -parameters




### -param pPipelineState [in, optional]

Type: <b><a href="https://msdn.microsoft.com/DD922194-8AD2-4ADF-9AC2-46C903C56AE6">ID3D12PipelineState</a>*</b>


            A pointer to the <a href="https://msdn.microsoft.com/DD922194-8AD2-4ADF-9AC2-46C903C56AE6">ID3D12PipelineState</a> object that contains the initial pipeline state for the command list.
          


## -returns




            Returns nothing.
          




## -remarks




        It is invalid to call <b>ClearState</b> on a bundle.  If an app calls <b>ClearState</b> on a bundle, the call to <a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a> will return <b>E_FAIL</b>.
      


        When <b>ClearState</b> is called, all currently bound resources are unbound.  The primitive topology is set to <a href="https://msdn.microsoft.com/b4becdcc-cc19-4d5a-940b-b232ebedce68">D3D_PRIMITIVE_TOPOLOGY_UNDEFINED</a>.  Viewports, scissor rectangles, stencil reference value, and the blend factor are set to empty values (all zeros).  Predication is disabled.
      


        The app-provided pipeline state object becomes bound as the currently set pipeline state object.
      




## -see-also




<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>
 

 

