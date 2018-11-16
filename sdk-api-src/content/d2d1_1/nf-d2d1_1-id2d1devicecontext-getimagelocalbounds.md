---
UID: NF:d2d1_1.ID2D1DeviceContext.GetImageLocalBounds
title: ID2D1DeviceContext::GetImageLocalBounds
author: windows-sdk-content
description: Gets the bounds of an image without the world transform of the context applied.
old-location: direct2d\id2d1devicecontext_getimagebounds.htm
tech.root: Direct2D
ms.assetid: 6a0f4e36-4490-4df5-a520-e10e524c8337
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetImageLocalBounds, GetImageLocalBounds method [Direct2D], GetImageLocalBounds method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],GetImageLocalBounds method, ID2D1DeviceContext.GetImageLocalBounds, ID2D1DeviceContext::GetImageLocalBounds, d2d1_1/ID2D1DeviceContext::GetImageLocalBounds, direct2d.id2d1devicecontext_getimagebounds
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID2D1DeviceContext.GetImageLocalBounds
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d2d1_1.h
: 
- ID2D1DeviceContext.GetImageLocalBounds
: 
---

# ID2D1DeviceContext::GetImageLocalBounds


## -description


Gets the bounds of an image without the world transform of the context applied.


## -parameters




### -param image [in]

Type: <b><a href="https://msdn.microsoft.com/9f7b4546-edbe-4000-a4ce-1a69563ebf9d">ID2D1Image</a>*</b>

The image whose bounds will be calculated.


### -param localBounds [out]

Type: <b><a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>[1]</b>

When this method returns, contains a pointer to the bounds of the image in device independent pixels (DIPs) and in local space.


## -returns



This method does not return a value.




## -remarks



The image bounds don't include multiplication by the world transform.  They do reflect the current DPI, unit mode, and interpolation mode of the context.  
      To get the bounds that include the world transform, use <a href="https://msdn.microsoft.com/939531E1-B641-48EF-B129-AC3AA5226919">ID2D1DeviceContext::GetImageWorldBounds</a>.

The returned bounds reflect which pixels would be impacted by calling <a href="https://msdn.microsoft.com/1235dd6d-8495-4a92-96b7-4d741d9e296f">DrawImage</a> with a 
      target offset of (0,0) and an identity world transform matrix. They do not reflect the current clip rectangle set on the device context or the extent of the context's current target image.




## -see-also




<a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>



<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>



<a href="https://msdn.microsoft.com/8292da6b-8232-4ef0-967d-a53d586aa9a9">ID2D1DeviceContext::CreateBitmap</a>



<a href="https://msdn.microsoft.com/939531E1-B641-48EF-B129-AC3AA5226919">ID2D1DeviceContext::GetImageWorldBounds</a>



<a href="https://msdn.microsoft.com/9f7b4546-edbe-4000-a4ce-1a69563ebf9d">ID2D1Image</a>
 

 

