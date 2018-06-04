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

# ID3D11ShaderReflectionVariable::GetInterfaceSlot


## -description


Gets the corresponding interface slot for a variable that represents an interface pointer.


## -parameters




### -param uArrayIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index of the array element to get the slot number for.  For a non-array variable this value will be zero.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Returns the index of the interface in the interface array.




## -remarks



GetInterfaceSlot gets the corresponding slot in an dynamic linkage array for an interface instance.  The returned slot number is used to set an interface instance to a particular class instance.  See the HLSL <a href="https://msdn.microsoft.com/124a358d-30ab-4efe-88ed-1ff277d17b25">Interfaces and Classes</a> overview for additional information.

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.


#### Examples


          Retrieving and using an interface slot
          

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
ID3D11ShaderReflectionVariable* pAmbientLightingVar = pReflector-&gt;GetVariableByName("g_abstractAmbientLighting");
g_iAmbientLightingOffset = pAmbientLightingVar-&gt;GetInterfaceSlot(0);
g_pPSClassLinkage-&gt;GetClassInstance( "g_hemiAmbientLight", 0, &amp;g_pHemiAmbientLightClass );
g_dynamicLinkageArray[g_iAmbientLightingOffset] = g_pHemiAmbientLightClass; 
...
pd3dImmediateContext-&gt;PSSetShader( g_pPixelShader, g_dynamicLinkageArray, g_iNumPSInterfaces );
      </pre>
</td>
</tr>
</table></span></div>
<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/4422a51f-b190-4df0-a1bb-a8ee2cc66da2">ID3D11ShaderReflectionVariable Interface</a>
 

 

