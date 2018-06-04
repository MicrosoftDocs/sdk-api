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

# ID3D12FunctionReflection interface


## -description



          A function-reflection interface accesses function info. 
          <div class="alert"><b>Note</b>  
            This interface is part of the HLSL shader linking technology that you can use on all Direct3D 12 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
          </div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12FunctionReflection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D12FunctionReflection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12FunctionReflection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4B953072-DEF0-4A30-93A1-247B0C2CAFA3">GetConstantBufferByIndex</a>
</td>
<td align="left" width="63%">
Gets a constant buffer by index for a function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AB781E44-2FCE-4E20-955C-C6F9F6F3064B">GetConstantBufferByName</a>
</td>
<td align="left" width="63%">

          Gets a constant buffer by name for a function.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CAFBC2D0-0C1C-4D55-87A4-C7ABB52976BF">GetDesc</a>
</td>
<td align="left" width="63%">

          Fills the function descriptor structure for the function.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88372A4E-596E-41F9-9FF4-9FD7E7F351DA">GetFunctionParameter</a>
</td>
<td align="left" width="63%">

          Gets the function parameter reflector.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DBABC959-0692-4DB9-9726-AFE6972A6B52">GetResourceBindingDesc</a>
</td>
<td align="left" width="63%">

          Gets a description of how a resource is bound to a function.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CF13496F-4317-4FFF-85CA-08FC64E320F4">GetResourceBindingDescByName</a>
</td>
<td align="left" width="63%">

          Gets a description of how a resource is bound to a function.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1E33C1B9-19DA-4ACD-8304-D5315AC63E2B">GetVariableByName</a>
</td>
<td align="left" width="63%">

          Gets a variable by name.
        

</td>
</tr>
</table> 


## -remarks




        To get a function-reflection interface, call <a href="https://msdn.microsoft.com/1600824A-6C9E-4C87-8D6B-07F299D47A53">ID3D12LibraryReflection::GetFunctionByIndex</a>. This isn't a COM interface, so you don't need to worry about reference counts or releasing the interface when you're done with it.
      

<div class="alert"><b>Note</b>  <b>ID3D12FunctionReflection</b> requires the D3dcompiler_47.dll or a later version of the DLL.
      </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/791d2c91-3791-47fe-b887-8117ecc798ba">Shader Interfaces</a>
 

 

