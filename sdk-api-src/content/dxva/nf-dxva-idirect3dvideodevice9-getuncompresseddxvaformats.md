---
UID: NF:dxva.IDirect3DVideoDevice9.GetUncompressedDXVAFormats
title: IDirect3DVideoDevice9::GetUncompressedDXVAFormats method
author: windows-driver-content
description: Gets a list of uncompressed pixel formats that can be rendered using a specified DirectX Video Acceleration (DXVA) profile.
old-location: mf\idirect3dvideodevice9_getuncompresseddxvaformats.htm
old-project: medfound
ms.assetid: 7c69ea5f-6054-4430-95b5-820db6854fc0
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetUncompressedDXVAFormats method [Media Foundation], GetUncompressedDXVAFormats method [Media Foundation], IDirect3DVideoDevice9 interface, GetUncompressedDXVAFormats,IDirect3DVideoDevice9.GetUncompressedDXVAFormats, IDirect3DVideoDevice9, IDirect3DVideoDevice9 interface [Media Foundation], GetUncompressedDXVAFormats method, IDirect3DVideoDevice9::GetUncompressedDXVAFormats, dxva/IDirect3DVideoDevice9::GetUncompressedDXVAFormats, mf.idirect3dvideodevice9_getuncompresseddxvaformats
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
-	IDirect3DVideoDevice9.GetUncompressedDXVAFormats
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDirect3DVideoDevice9::GetUncompressedDXVAFormats method


## -description


Gets a list of uncompressed pixel formats that can be rendered using a specified DirectX Video Acceleration (DXVA) profile.


## -parameters




### -param pGuid

Pointer to a GUID that specifies the DXVA profile. To get a list of supported profiles, call <a href="https://msdn.microsoft.com/4adbbac2-a25d-4e17-b62e-a02a67dcdbed">IDirect3DVideoDevice9::GetDXVAGuids</a>.


### -param pNumFormats

On input, specifies the number of elements in the <i>pFormats</i> array.
            If <i>pFormats</i> is <b>NULL</b>, the value of <code>*pNumFormats</code> must be zero.

On output, if <i>pFormats</i> is <b>NULL</b>, <i>pNumFormats</i> receives the number of supported pixel formats. Otherwise, <i>pNumFormats</i> receives the actual number of pixel formats copied to the <i>pFormats</i> array.


### -param pFormats


            Address of an array of <b>D3DFORMAT</b> values, or <b>NULL</b>. If the value is non-<b>NULL</b>, the array receives a list of pixel formats.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call this method twice. On the first call, set <i>pFormats</i> to <b>NULL</b>. The <i>pNumFormats</i> parameter receives the number of formats. Allocate a <b>D3DFORMAT</b> array with the required size, and call the method again. This time, set <i>pFormats</i> to the address of the array. The method fills the array with the list of pixel formats.

The driver should return the formats in decreasing order of preference, with the most preferred format listed first.




## -see-also




<a href="https://msdn.microsoft.com/abe3beac-f3f8-413d-8b83-9da3340b19ac">IDirect3DVideoDevice9</a>
 

 

