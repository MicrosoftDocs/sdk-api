---
UID: NF:d2d1_1.ID2D1DeviceContext.SetPrimitiveBlend
title: ID2D1DeviceContext::SetPrimitiveBlend (d2d1_1.h)
author: windows-sdk-content
description: Changes the primitive blend mode that is used for all rendering operations in the device context.
old-location: direct2d\id2d1devicecontext_setprimitiveblend.htm
tech.root: Direct2D
ms.assetid: be04c9f7-397f-468e-91c0-3b11c68b489f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1DeviceContext interface [Direct2D],SetPrimitiveBlend method, ID2D1DeviceContext.SetPrimitiveBlend, ID2D1DeviceContext::SetPrimitiveBlend, SetPrimitiveBlend, SetPrimitiveBlend method [Direct2D], SetPrimitiveBlend method [Direct2D],ID2D1DeviceContext interface, d2d1_1/ID2D1DeviceContext::SetPrimitiveBlend, direct2d.id2d1devicecontext_setprimitiveblend
ms.topic: method
req.header: d2d1_1.h
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
req.lib: 
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DeviceContext.SetPrimitiveBlend
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1DeviceContext::SetPrimitiveBlend


## -description


Changes the primitive blend mode that is used for all rendering operations in the device context.


## -parameters




### -param primitiveBlend

Type: <b><a href="https://msdn.microsoft.com/411a42c9-f8d7-46f3-a6e6-51afc83375ad">D2D1_PRIMITIVE_BLEND</a></b>

The primitive blend to use.


## -returns



This method does not return a value.




## -remarks



The primitive blend will apply to all of the primitive drawn on the context, unless this is overridden with the <i>compositeMode</i> parameter on the <a href="https://msdn.microsoft.com/c41d8a79-280a-451e-b07b-f904d07da5c7">DrawImage</a> API.

The primitive blend applies to the interior of any primitives drawn on the context. In the case of <a href="https://msdn.microsoft.com/c41d8a79-280a-451e-b07b-f904d07da5c7">DrawImage</a>, this will be implied by the image rectangle, offset and world transform.

If the primitive blend is anything other than <b>D2D1_PRIMITIVE_BLEND_SOURCE_OVER</b> then ClearType rendering will be turned off. If the application explicitly forces ClearType rendering in these modes, the drawing context will be placed in an error state. D2DERR_WRONG_STATE will be returned from either <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a> or <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">Flush</a>.





## -see-also




<a href="https://msdn.microsoft.com/411a42c9-f8d7-46f3-a6e6-51afc83375ad">D2D1_PRIMITIVE_BLEND</a>



<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>
 

 

