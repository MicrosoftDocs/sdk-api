---
UID: NF:d3d11.ID3D11DeviceContext.PSGetShader
title: ID3D11DeviceContext::PSGetShader method
author: windows-driver-content
description: Get the pixel shader currently set on the device.
old-location: direct3d11\id3d11devicecontext_psgetshader.htm
old-project: direct3d11
ms.assetid: 6ebeb763-b517-468c-bd46-022a426e0b6e
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: 670956b7-c83d-77ff-bc7b-f0c5ef8d9986, ID3D11DeviceContext, ID3D11DeviceContext interface [Direct3D 11], PSGetShader method, ID3D11DeviceContext::PSGetShader, PSGetShader method [Direct3D 11], PSGetShader method [Direct3D 11], ID3D11DeviceContext interface, PSGetShader,ID3D11DeviceContext.PSGetShader, d3d11/ID3D11DeviceContext::PSGetShader, direct3d11.id3d11devicecontext_psgetshader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
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
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11DeviceContext.PSGetShader
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::PSGetShader method


## -description



      Get the pixel shader currently set on the device.


## -parameters




### -param ppPixelShader [out]

Type: <b><a href="https://msdn.microsoft.com/d16e00a9-02f9-413f-b9f7-31446fb0a692">ID3D11PixelShader</a>**</b>


            Address of a pointer to a pixel shader (see <a href="https://msdn.microsoft.com/d16e00a9-02f9-413f-b9f7-31446fb0a692">ID3D11PixelShader</a>) to be returned by the method.
          


### -param ppClassInstances [out, optional]

Type: <b><a href="https://msdn.microsoft.com/70d006d2-5c47-4e8a-9a14-b5475d88ac32">ID3D11ClassInstance</a>**</b>


            Pointer to an array of class instance interfaces (see <a href="https://msdn.microsoft.com/70d006d2-5c47-4e8a-9a14-b5475d88ac32">ID3D11ClassInstance</a>).
          


### -param pNumClassInstances [in, out, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>


            The number of class-instance elements in the array.
          


## -returns




            Returns nothing.
          




## -remarks




          Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed, to avoid memory leaks.
        

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

