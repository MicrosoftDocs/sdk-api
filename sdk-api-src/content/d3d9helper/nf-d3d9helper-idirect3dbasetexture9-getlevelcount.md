---
UID: NF:d3d9helper.IDirect3DBaseTexture9.GetLevelCount
title: IDirect3DBaseTexture9::GetLevelCount
author: windows-sdk-content
description: Returns the number of texture levels in a multilevel texture.
old-location: direct3d9\idirect3dbasetexture9__getlevelcount.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dbasetexture9__getlevelcount.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: GetLevelCount, GetLevelCount method [Direct3D 9], GetLevelCount method [Direct3D 9],IDirect3DBaseTexture9 interface, IDirect3DBaseTexture9 interface [Direct3D 9],GetLevelCount method, IDirect3DBaseTexture9.GetLevelCount, IDirect3DBaseTexture9::GetLevelCount, d1e2b647-f3f4-ac84-e24e-feeb8e0c6bf8, d3d9helper/IDirect3DBaseTexture9::GetLevelCount, direct3d9.idirect3dbasetexture9__getlevelcount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9helper.h
req.include-header: D3D9.h
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
req.typenames: D3DVSHADERCAPS2_0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DBaseTexture9.GetLevelCount
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DBaseTexture9::GetLevelCount


## -description


Returns the number of texture levels in a multilevel texture.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

A <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a> value that indicates the number of texture levels in a multilevel texture.




## -remarks



<div class="alert"><b>Warning</b>  If you create a texture with <a href="d3dusage.htm">D3DUSAGE_AUTOGENMIPMAP</a> to make that texture automatically generate sublevels, <b>GetLevelCount</b> always returns 1 for the number of levels.</div>
<div> </div>
This method applies to the following interfaces, which inherit from <a href="https://msdn.microsoft.com/d4d7f8b9-2e7b-4445-8380-2d321a46e064">IDirect3DBaseTexture9</a>.

<ul>
<li>
<a href="https://msdn.microsoft.com/59e400ae-d2ec-425c-9adf-49cb5a24c808">IDirect3DCubeTexture9</a>
</li>
<li>
<a href="https://msdn.microsoft.com/fcea1048-1d9b-409f-9b5a-cdf85c30c76e">IDirect3DTexture9</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c92cabb8-61d1-4dcf-acf1-fddd3e007d47">IDirect3DVolumeTexture9</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/d4d7f8b9-2e7b-4445-8380-2d321a46e064">IDirect3DBaseTexture9</a>
 

 

