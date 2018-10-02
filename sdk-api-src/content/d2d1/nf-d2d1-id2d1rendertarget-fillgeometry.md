---
UID: NF:d2d1.ID2D1RenderTarget.FillGeometry
title: ID2D1RenderTarget::FillGeometry
author: windows-sdk-content
description: Paints the interior of the specified geometry.
old-location: direct2d\ID2D1RenderTarget_FillGeometry.htm
tech.root: direct2d
ms.assetid: 097f21ac-a062-4ce1-bdc7-87317dbdf5be
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: FillGeometry, FillGeometry method [Direct2D], FillGeometry method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],FillGeometry method, ID2D1RenderTarget.FillGeometry, ID2D1RenderTarget::FillGeometry, d2d1/ID2D1RenderTarget::FillGeometry, direct2d.ID2D1RenderTarget_FillGeometry
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - ID2D1RenderTarget.FillGeometry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::FillGeometry


## -description


Paints the interior of the specified geometry.


## -parameters




### -param geometry [in]

Type: <b><a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>*</b>

The geometry to paint.


### -param brush [in]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

The brush used to paint the geometry's interior.


### -param opacityBrush [in, optional]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

The opacity mask to apply to the geometry, or <b>NULL</b> for no opacity mask. If an opacity mask (the <i>opacityBrush</i> parameter) is specified, <i>brush</i> must be an <a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a> that has   its x- and y-extend modes set to <a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE_CLAMP</a>. For more information, see the Remarks section. 


## -returns



This method does not return a value.




## -remarks



If the <i>opacityBrush</i> parameter is not <b>NULL</b>, the alpha value of each pixel of the mapped <i>opacityBrush</i> is used to determine the resulting opacity of each corresponding pixel of the geometry. Only the alpha value of each color in the brush is used for this processing; all other color information is ignored. 

The alpha value specified by the brush is multiplied by the alpha value of the geometry after the geometry has been painted by <i>brush</i>.  


When this method fails, it does not return an error code. To determine whether a drawing operation (such as <b>FillGeometry</b>) failed, check the result returned by the <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">ID2D1RenderTarget::EndDraw</a> or <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">ID2D1RenderTarget::Flush</a> method. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/d7aad487-04e0-448d-bedf-b8dfadc7bbe9">How to Draw and Fill a Complex Shape</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/f1a14447-39fa-4a48-9516-ff5b03abc3a6">D2D1_FILL_MODE</a>



<a href="https://msdn.microsoft.com/aaf16fa7-23fd-4020-ae4c-b7832040732d">Geometries</a>



<a href="https://msdn.microsoft.com/f5870d4b-dd30-4034-884e-1c398a6865c6">Geometries Overview</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

