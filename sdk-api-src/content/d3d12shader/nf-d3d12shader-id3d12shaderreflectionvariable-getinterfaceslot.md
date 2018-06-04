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

# ID3D12ShaderReflectionVariable::GetInterfaceSlot


## -description



          Gets the corresponding interface slot for a variable that represents an interface pointer.
        


## -parameters




### -param uArrayIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


            The index of the array element to get the slot number for.
            For a non-array variable this value will be zero.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


            Returns the index of the interface in the interface array.
          




## -remarks



GetInterfaceSlot gets the corresponding slot in an dynamic linkage array for an interface instance.
          The returned slot number is used to set an interface instance to a particular class instance.
          See the HLSL <a href="https://msdn.microsoft.com/124a358d-30ab-4efe-88ed-1ff277d17b25">Interfaces and Classes</a> overview for additional information.
        


        This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.
      




## -see-also




<a href="https://msdn.microsoft.com/E4CF0C77-2792-46DC-B38F-22C0ACBFD615">ID3D12ShaderReflectionVariable</a>
 

 

