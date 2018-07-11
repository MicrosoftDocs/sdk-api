---
UID: NF:d3d11_3.ID3D11Device3.CreateDeferredContext3
title: ID3D11Device3::CreateDeferredContext3
author: windows-sdk-content
description: Creates a deferred context, which can record command lists.
old-location: direct3d11\id3d11device3_createdeferredcontext3.htm
old-project: direct3d11
ms.assetid: 78B52E38-3256-4151-96DA-4C81A2A516CF
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: CreateDeferredContext3, CreateDeferredContext3 method [Direct3D 11], CreateDeferredContext3 method [Direct3D 11],ID3D11Device3 interface, ID3D11Device3 interface [Direct3D 11],CreateDeferredContext3 method, ID3D11Device3.CreateDeferredContext3, ID3D11Device3::CreateDeferredContext3, d3d11_3/ID3D11Device3::CreateDeferredContext3, direct3d11.id3d11device3_createdeferredcontext3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11_3.h
req.include-header: 
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
req.typenames: D3D11_TEXTURE_LAYOUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device3.CreateDeferredContext3
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Device3::CreateDeferredContext3


## -description



          Creates a deferred context, which can record <a href="https://msdn.microsoft.com/4f581bc7-6c5e-4e56-b768-7f3cc5dbcb3e">command lists</a>.
        


## -parameters




### -param ContextFlags

Type: <b>UINT</b>


            Reserved for future use.  Pass 0.
          


### -param ppDeferredContext [out, optional]

Type: <b>ID3D11DeviceContext3**</b>


            Upon completion of the method, the passed pointer to an <a href="https://msdn.microsoft.com/65F462DB-5546-4B23-B438-60067FD60103">ID3D11DeviceContext3</a> interface pointer is initialized.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


              Returns S_OK if successful; otherwise, returns one of the following:
            

<ul>
<li>
                Returns <b>DXGI_ERROR_DEVICE_REMOVED</b> if the video card has been physically removed from the system, or a driver upgrade for the video card has occurred.
                If this error occurs, you should destroy and recreate the device.
              </li>
<li>
                Returns <b>DXGI_ERROR_INVALID_CALL</b> if the
                <b>CreateDeferredContext3</b>
                method can't be called from the current context.
                For example, if the device was created with the <a href="https://msdn.microsoft.com/580c784a-17de-495c-9159-833f858ad155">D3D11_CREATE_DEVICE_SINGLETHREADED</a> value,  <b>CreateDeferredContext3</b> returns <b>DXGI_ERROR_INVALID_CALL</b>.
              </li>
<li>
                Returns <b>E_INVALIDARG</b> if the <i>ContextFlags</i> parameter is invalid.
              </li>
<li>
                Returns <b>E_OUTOFMEMORY</b> if the app has exhausted available memory.
              </li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/2F7E343F-2A25-44F2-9352-5F378718D6F6">ID3D11Device1::CreateDeferredContext1</a>



<a href="https://msdn.microsoft.com/57901FAC-428C-437B-9C9B-2DB2D16049F8">ID3D11Device2::CreateDeferredContext2</a>



<a href="https://msdn.microsoft.com/0AA10851-0077-4075-BD41-72FCD7BC0556">ID3D11Device3</a>



<a href="https://msdn.microsoft.com/fbf01844-eaf1-4360-833e-c95ba686fff5">ID3D11Device::CreateDeferredContext</a>
 

 

