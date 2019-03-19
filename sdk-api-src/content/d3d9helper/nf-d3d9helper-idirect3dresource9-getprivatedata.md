---
UID: NF:d3d9helper.IDirect3DResource9.GetPrivateData
title: IDirect3DResource9::GetPrivateData (d3d9helper.h)
author: windows-sdk-content
description: Copies the private data associated with the resource to a provided buffer.
old-location: direct3d9\idirect3dresource9__getprivatedata.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dresource9__getprivatedata.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetPrivateData, GetPrivateData method [Direct3D 9], GetPrivateData method [Direct3D 9],IDirect3DResource9 interface, IDirect3DResource9 interface [Direct3D 9],GetPrivateData method, IDirect3DResource9.GetPrivateData, IDirect3DResource9::GetPrivateData, a3ce4b5e-f58e-cf26-2ef5-896eaf4a5613, d3d9helper/IDirect3DResource9::GetPrivateData, direct3d9.idirect3dresource9__getprivatedata
ms.topic: method
req.header: d3d9helper.h
req.include-header: D3D9.h
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DResource9.GetPrivateData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DResource9::GetPrivateData


## -description


Copies the private data associated with the resource to a provided buffer.


## -parameters




### -param refguid [in]

Type: <b><a href="http://go.microsoft.com/?linkid=9742306">REFGUID</a></b>

The globally unique identifier that identifies the private data to retrieve. 


### -param pData [in, out]

Type: <b>void*</b>

Pointer to a previously allocated buffer to fill with the requested private data if the call succeeds. The application calling this method is responsible for allocating and releasing this buffer. If this parameter is <b>NULL</b>, this method will return the buffer size in pSizeOfData.


### -param pSizeOfData [in, out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

Pointer to the size of the buffer at 
    pData, in bytes. If this value is less than the actual size of the private data (such as 0), the method sets this parameter to the required buffer size and the method returns D3DERR_MOREDATA. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, D3DERR_MOREDATA, D3DERR_NOTFOUND.




## -remarks



This method is inherited by the following interfaces: 
    
    <a href="https://msdn.microsoft.com/en-us/library/Bb205878(v=VS.85).aspx">IDirect3DResource9</a>, 
    
    <a href="https://msdn.microsoft.com/en-us/library/Bb174322(v=VS.85).aspx">IDirect3DBaseTexture9</a>,
    
    <a href="https://msdn.microsoft.com/en-us/library/Bb174329(v=VS.85).aspx">IDirect3DCubeTexture9</a>, 
    
    <a href="https://msdn.microsoft.com/en-us/library/Bb205909(v=VS.85).aspx">IDirect3DTexture9</a>, 
    
    <a href="https://msdn.microsoft.com/en-us/library/Bb205941(v=VS.85).aspx">IDirect3DVolumeTexture9</a>,
    
    <a href="https://msdn.microsoft.com/en-us/library/Bb205865(v=VS.85).aspx">IDirect3DIndexBuffer9</a>, 
    
    <a href="https://msdn.microsoft.com/en-us/library/Bb205915(v=VS.85).aspx">IDirect3DVertexBuffer9</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205878(v=VS.85).aspx">IDirect3DResource9</a>
 

 

