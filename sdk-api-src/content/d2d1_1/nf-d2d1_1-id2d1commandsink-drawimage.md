---
UID: NF:d2d1_1.ID2D1CommandSink.DrawImage
title: ID2D1CommandSink::DrawImage (d2d1_1.h)
author: windows-sdk-content
description: Draws the provided image to the command sink.
old-location: direct2d\id2d1commandsink_drawimage.htm
tech.root: Direct2D
ms.assetid: 1235dd6d-8495-4a92-96b7-4d741d9e296f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrawImage, DrawImage method [Direct2D], DrawImage method [Direct2D],ID2D1CommandSink interface, ID2D1CommandSink interface [Direct2D],DrawImage method, ID2D1CommandSink.DrawImage, ID2D1CommandSink::DrawImage, d2d1_1/ID2D1CommandSink::DrawImage, direct2d.id2d1commandsink_drawimage
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
 - ID2D1CommandSink.DrawImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1CommandSink::DrawImage


## -description


Draws the provided image to the command sink.  


## -parameters




### -param image [in]

Type: <b><a href="https://msdn.microsoft.com/9f7b4546-edbe-4000-a4ce-1a69563ebf9d">ID2D1Image</a>*</b>

The image to be drawn to the command sink.


### -param targetOffset [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a>*</b>

This defines the offset in the destination space that the image will be rendered to. The entire logical extent of the image will be rendered to the corresponding destination. If not specified, the destination origin will be (0, 0). The top-left corner of the image will be mapped to the target offset. This will not necessarily be the origin.


### -param imageRectangle [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

The corresponding rectangle in the image space will be mapped to the provided origins when processing the image.


### -param interpolationMode

Type: <b><a href="https://msdn.microsoft.com/7a32f551-afad-4eb2-953f-a9acc71d7776">D2D1_INTERPOLATION_MODE</a></b>

The interpolation mode to use to  scale the image if necessary.



### -param compositeMode

Type: <b><a href="https://msdn.microsoft.com/4f01e805-aed7-4bfc-9793-42a9fdde3473">D2D1_COMPOSITE_MODE</a></b>

If specified, the composite mode that will be applied to the limits of the currently selected clip.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code. 





## -remarks



Because the image can itself be a command list or contain an effect graph that in turn contains a command list, this method can result in recursive processing.




## -see-also




<a href="https://msdn.microsoft.com/52e6da86-c7c6-48e7-b0ff-a54770663f14">ID2D1CommandList::Stream</a>



<a href="https://msdn.microsoft.com/4e0ce837-7f4e-4b93-8dd7-68f60cfb1105">ID2D1CommandSink</a>



<a href="https://msdn.microsoft.com/c41d8a79-280a-451e-b07b-f904d07da5c7">ID2D1DeviceContext::DrawImage</a>
 

 

