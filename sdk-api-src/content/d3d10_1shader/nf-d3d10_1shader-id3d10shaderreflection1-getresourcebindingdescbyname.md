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

# ID3D10ShaderReflection1::GetResourceBindingDescByName


## -description


Gets a resource binding description by name.


## -parameters




### -param Name [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a>*</b>

A pointer to a string containing the variable name.


### -param pDesc

Type: <b><a href="https://msdn.microsoft.com/8929f7d4-6fd0-4b48-b1d8-0b089d4c730d">D3D10_SHADER_INPUT_BIND_DESC</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/8929f7d4-6fd0-4b48-b1d8-0b089d4c730d">D3D10_SHADER_INPUT_BIND_DESC</a> structure that will be populated with resource binding information.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



This method requires Windows Vista Service Pack 1.




## -see-also




<a href="https://msdn.microsoft.com/344a0bf2-3ad8-4c58-b4d8-de386fdfd1c2">ID3D10ShaderReflection1 Interface</a>
 

 

