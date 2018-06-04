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

# IDirect3DVolume9::LockBox


## -description


Locks a box on a volume resource.


## -parameters




### -param pLockedVolume [out]

Type: <b><a href="https://msdn.microsoft.com/b371fb5e-2d65-453c-acd7-214de8aaa78a">D3DLOCKED_BOX</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/b371fb5e-2d65-453c-acd7-214de8aaa78a">D3DLOCKED_BOX</a> structure, describing the locked region. 


### -param pBox [in]

Type: <b>const <a href="https://msdn.microsoft.com/415a96bc-1621-4691-b87a-98ca22f0bf07">D3DBOX</a>*</b>

Pointer to a box to lock. Specified by a pointer to a <a href="https://msdn.microsoft.com/415a96bc-1621-4691-b87a-98ca22f0bf07">D3DBOX</a> structure. Specifying <b>NULL</b> for this parameter locks the entire volume. 


### -param Flags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Combination of zero or more locking flags that describe the type of lock to perform. For this method, the valid flags are: 
    


<ul>
<li>D3DLOCK_DISCARD</li>
<li>D3DLOCK_NO_DIRTY_UPDATE</li>
<li>D3DLOCK_NOSYSLOCK</li>
<li>D3DLOCK_READONLY</li>
</ul>

For a description of the flags, see <a href="https://msdn.microsoft.com/46a611bd-a1ec-4967-b68d-72661d1b5cad">D3DLOCK</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



For performance reasons, dirty regions are only recorded for level zero of a texture. Dirty regions are automatically recorded when <b>IDirect3DVolume9::LockBox</b> is called without D3DLOCK_NO_DIRTY_UPDATE or D3DLOCK_READONLY. See <a href="https://msdn.microsoft.com/79be31d9-0dd2-416c-b58c-9b3b7777c65c">IDirect3DDevice9::UpdateTexture</a> for more information.




## -see-also




<a href="https://msdn.microsoft.com/b157d2d1-5813-43a1-ac3a-000b13b1bb62">IDirect3DVolume9</a>



<a href="https://msdn.microsoft.com/5055ca1d-40d9-4074-830d-3432e6ea1018">IDirect3DVolume9::UnlockBox</a>
 

 

