---
UID: NF:d2d1effectauthor.ID2D1DrawInfo.SetPixelShader
title: ID2D1DrawInfo::SetPixelShader
author: windows-sdk-content
description: Set the shader instructions for this transform.
old-location: direct2d\id2d1drawinfo_setpixelshader.htm
tech.root: direct2d
ms.assetid: 9CB38592-6B49-48FE-AA3F-1FC402489454
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: ID2D1DrawInfo interface [Direct2D],SetPixelShader method, ID2D1DrawInfo.SetPixelShader, ID2D1DrawInfo::SetPixelShader, SetPixelShader, SetPixelShader method [Direct2D], SetPixelShader method [Direct2D],ID2D1DrawInfo interface, d2d1effectauthor/ID2D1DrawInfo::SetPixelShader, direct2d.id2d1drawinfo_setpixelshader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1DrawInfo.SetPixelShader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DrawInfo::SetPixelShader


## -description


Set the shader instructions for this transform.


## -parameters




### -param shaderId [in]

Type: <b>REFGUID</b>

The resource id for the  shader.


### -param pixelOptions

Type: <b><a href="https://msdn.microsoft.com/285cf526-d8f6-4ae7-a017-066e397078b0">D2D1_PIXEL_OPTIONS</a></b>

Additional information provided to the renderer to indicate the operations the pixel shader does.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



 If this call fails, the corresponding <a href="https://msdn.microsoft.com/e90d1830-c356-48f1-ac7b-1d94c8c26569">ID2D1Effect</a> instance is placed into an error state and will fail to Draw, it will place the context into an error state which can be retrieved through the <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">ID2D1DeviceContext::EndDraw</a> call.



Specifying <i>pixelOptions</i> other than D2D1_PIXEL_OPTIONS_NONE can enable the renderer to perform certain optimizations such as combining various parts of the effect graph together. If this information does not accurately describe the shader, indeterminate rendering artifacts can result.





## -see-also




<a href="https://msdn.microsoft.com/9C7B8CE0-0D2D-4383-9BE1-25F86BCEF253">ID2D1DrawInfo</a>
 

 

