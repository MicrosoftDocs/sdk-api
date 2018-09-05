---
UID: NF:d3d11.ID3D11Device.CreateClassLinkage
title: ID3D11Device::CreateClassLinkage
author: windows-sdk-content
description: Creates class linkage libraries to enable dynamic shader linkage.
old-location: direct3d11\id3d11device_createclasslinkage.htm
old-project: direct3d11
ms.assetid: 1d68e977-bcdc-4aab-9434-29200553a69e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 411c8228-de78-2b45-6754-17ebcd3ef8de, CreateClassLinkage, CreateClassLinkage method [Direct3D 11], CreateClassLinkage method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateClassLinkage method, ID3D11Device.CreateClassLinkage, ID3D11Device::CreateClassLinkage, d3d11/ID3D11Device::CreateClassLinkage, direct3d11.id3d11device_createclasslinkage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.redist: 
req.target-type: Windows
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
tech.root: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device.CreateClassLinkage
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Device::CreateClassLinkage


## -description


Creates class linkage libraries to enable dynamic shader linkage.


## -parameters




### -param ppLinkage [out]

Type: <b><a href="https://msdn.microsoft.com/eac03911-d881-4304-9598-912321ac0b0c">ID3D11ClassLinkage</a>**</b>

A pointer to a class-linkage interface pointer (see <a href="https://msdn.microsoft.com/eac03911-d881-4304-9598-912321ac0b0c">ID3D11ClassLinkage</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



The <a href="https://msdn.microsoft.com/eac03911-d881-4304-9598-912321ac0b0c">ID3D11ClassLinkage</a> interface returned in <i>ppLinkage</i> is associated with a shader by passing it as a parameter to one of the <a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a> create shader methods such as <a href="https://msdn.microsoft.com/f013a648-fd11-417b-8f87-36a4be901715">ID3D11Device::CreatePixelShader</a>.


#### Examples

Using CreateClassLinkage
          

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
ID3D11ClassLinkage * g_pPSClassLinkage = NULL;            
pd3dDevice-&gt;CreateClassLinkage( &amp;g_pPSClassLinkage ); 
          </pre>
</td>
</tr>
</table></span></div>
<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
 

 

