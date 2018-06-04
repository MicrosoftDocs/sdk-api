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

# ID3D12ShaderReflection::GetThreadGroupSize


## -description



          Retrieves the sizes, in units of threads, of the X, Y, and Z dimensions of the shader's thread-group grid.
        


## -parameters




### -param pSizeX [out, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>


            A pointer to the size, in threads, of the x-dimension of the thread-group grid. The maximum size is 1024.
          


### -param pSizeY [out, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>


            A pointer to the size, in threads, of the y-dimension of the thread-group grid. The maximum size is 1024.
          


### -param pSizeZ [out, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>


            A pointer to the size, in threads, of the z-dimension of the thread-group grid. The maximum size is 64.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


            Returns the total size, in threads, of the thread-group grid by calculating the product of the size of each dimension.
            

<pre class="syntax" xml:space="preserve"><code>*pSizeX * *pSizeY * *pSizeZ;</code></pre>



## -remarks




          This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.
        

When a compute shader is written it defines the actions of a single thread group only. If multiple thread groups are required, it is the role of the <a href="https://msdn.microsoft.com/948EE430-6B34-473D-9B5F-1C78CECFBF6F">ID3D12GraphicsCommandList::Dispatch</a> call to issue multiple thread groups. 




## -see-also




<a href="https://msdn.microsoft.com/145F2CCB-C076-42BE-8AF4-74349CDF6B02">ID3D12ShaderReflection</a>
 

 

