---
UID: NF:d2d1.ID2D1RenderTarget.DrawGeometry
title: ID2D1RenderTarget::DrawGeometry
author: windows-sdk-content
description: Draws the outline of the specified geometry using the specified stroke style.
old-location: direct2d\ID2D1RenderTarget_DrawGeometry.htm
tech.root: direct2d
ms.assetid: 319b2680-34f8-4e00-985e-47ff87115794
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DrawGeometry, DrawGeometry method [Direct2D], DrawGeometry method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],DrawGeometry method, ID2D1RenderTarget.DrawGeometry, ID2D1RenderTarget::DrawGeometry, d2d1/ID2D1RenderTarget::DrawGeometry, direct2d.ID2D1RenderTarget_DrawGeometry
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
 - ID2D1RenderTarget.DrawGeometry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::DrawGeometry


## -description


Draws the outline of the specified geometry using the specified stroke style.


## -parameters




### -param geometry [in]

Type: <b><a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>*</b>

The geometry to draw.


### -param brush [in]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

The brush used to paint the geometry's stroke.


### -param strokeWidth

Type: <b>FLOAT</b>

The width of the stroke, in device-independent pixels. The value must be greater than or equal to 0.0f. If this parameter isn't specified, it defaults to 1.0f. The stroke is centered on the line.


### -param strokeStyle [in, optional]

Type: <b><a href="https://msdn.microsoft.com/2cdf66dc-f34f-4132-8c06-7464648d3cef">ID2D1StrokeStyle</a>*</b>

The style of stroke to apply to the geometry's outline, or <b>NULL</b> to paint a solid stroke.


## -returns



This method does not return a value.




## -remarks



This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <b>DrawGeometry</b>) failed, check the result returned by the <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">ID2D1RenderTarget::EndDraw</a> or <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">ID2D1RenderTarget::Flush</a> methods. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/d7aad487-04e0-448d-bedf-b8dfadc7bbe9">How to Draw and Fill a Complex Shape</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/aaf16fa7-23fd-4020-ae4c-b7832040732d">Geometries</a>



<a href="https://msdn.microsoft.com/f5870d4b-dd30-4034-884e-1c398a6865c6">Geometries Overview</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

