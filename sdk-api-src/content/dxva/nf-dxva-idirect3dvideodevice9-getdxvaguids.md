---
UID: NF:dxva.IDirect3DVideoDevice9.GetDXVAGuids
title: IDirect3DVideoDevice9::GetDXVAGuids method
author: windows-driver-content
description: Gets a list of DirectX Video Acceleration (DXVA) profiles that are supported by the display driver.
old-location: mf\idirect3dvideodevice9_getdxvaguids.htm
old-project: medfound
ms.assetid: 4adbbac2-a25d-4e17-b62e-a02a67dcdbed
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetDXVAGuids method [Media Foundation], GetDXVAGuids method [Media Foundation], IDirect3DVideoDevice9 interface, GetDXVAGuids,IDirect3DVideoDevice9.GetDXVAGuids, IDirect3DVideoDevice9, IDirect3DVideoDevice9 interface [Media Foundation], GetDXVAGuids method, IDirect3DVideoDevice9::GetDXVAGuids, dxva/IDirect3DVideoDevice9::GetDXVAGuids, mf.idirect3dvideodevice9_getdxvaguids
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxva.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: COPP_TVProtectionStandard
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dxva.h
api_name:
-	IDirect3DVideoDevice9.GetDXVAGuids
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDirect3DVideoDevice9::GetDXVAGuids method


## -description


Gets a list of DirectX Video Acceleration (DXVA) profiles that are supported by the display driver.


## -parameters




### -param pNumGuids

On input, specifies the number of elements in the <i>pGuids</i> array.
            If <i>pGuids</i> is <b>NULL</b>, the value of <code>*pNumGuids</code> must be zero. 

On output, if <i>pGuids</i> is <b>NULL</b>, <i>pNumGuids</i> receives the number of restricted-mode DXVA profiles. Otherwise, <i>pNumGuids</i> receives the actual number of GUIDs that are copied to the <i>pGuids</i> array.


### -param pGuids


            Address of an array of GUIDs or <b>NULL</b>. If the value is non-<b>NULL</b>, the array receives a list of GUIDs that specify restricted-mode DXVA profiles. These GUIDs are defined in dxva.h, and are documented in the <a href="http://go.microsoft.com/fwlink/p/?linkid=93647">DXVA 1.0 specification</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call this method twice. On the first call, set <i>pGuids</i> to <b>NULL</b>. The <i>pNumGuids</i> parameter receives the number of DXVA profile GUIDs. Allocate an array of GUIDs with the required size and call the method again. This time, set <i>pGuids</i> to the address of the array. The method fills the array with the list of DXVA profile GUIDs.




## -see-also




<a href="https://msdn.microsoft.com/abe3beac-f3f8-413d-8b83-9da3340b19ac">IDirect3DVideoDevice9</a>
 

 

