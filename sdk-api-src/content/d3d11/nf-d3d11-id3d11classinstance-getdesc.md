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

# ID3D11ClassInstance::GetDesc


## -description


Gets a description of the current HLSL class.


## -parameters




### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/8ed0e6dd-227b-4e15-b949-34086523f064">D3D11_CLASS_INSTANCE_DESC</a>*</b>


            A pointer to a <a href="https://msdn.microsoft.com/8ed0e6dd-227b-4e15-b949-34086523f064">D3D11_CLASS_INSTANCE_DESC</a> structure that describes the current HLSL class.
          


## -returns



This method does not return a value.




## -remarks




          For more information about using the <a href="https://msdn.microsoft.com/70d006d2-5c47-4e8a-9a14-b5475d88ac32">ID3D11ClassInstance</a> interface, see
          <a href="https://msdn.microsoft.com/2f5f7852-0f0a-4fad-a412-9a0d634c73b6">Dynamic Linking</a>.
        


          An instance is not restricted to being used for a single type in a single shader. An instance is flexible and can be used for any shader that used the same type name or instance name when the instance was generated.
        

<ul>
<li>
            A created instance will work for any shader that contains a type of the same type name.
            For instance, a class instance created with the type name <b>DefaultShader</b> would work in any shader that contained a type <b>DefaultShader</b>
            even though several shaders could describe a different type.
          </li>
<li>
            A gotten instance maps directly to an instance name/index in a shader.
            A class instance aquired using GetClassInstance will work for any shader that contains a class instance of the name used to generate the runtime instance, the instance does not have to be the same type in all of the shaders it's used in.
          </li>
</ul>

          An instance does not replace the importance of reflection for a particular shader since a gotten instance will not know its slot location and a created instance only specifies a type name.
        

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/70d006d2-5c47-4e8a-9a14-b5475d88ac32">ID3D11ClassInstance</a>
 

 

