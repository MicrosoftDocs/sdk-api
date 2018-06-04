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

# ID3D11ShaderReflectionType::GetDesc


## -description


Get the description of a shader-reflection-variable type.


## -parameters




### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/8d2067a3-17f8-4496-a613-581f5e35fe93">D3D11_SHADER_TYPE_DESC</a>*</b>

A pointer to a shader-type description (see <a href="https://msdn.microsoft.com/8d2067a3-17f8-4496-a613-581f5e35fe93">D3D11_SHADER_TYPE_DESC</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.




## -see-also




<a href="https://msdn.microsoft.com/04520be2-2491-4f10-988a-e203659efddf">ID3D11ShaderReflectionType Interface</a>
 

 

