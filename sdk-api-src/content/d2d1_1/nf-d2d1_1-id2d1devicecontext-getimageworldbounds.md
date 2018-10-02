---
UID: NF:d2d1_1.ID2D1DeviceContext.GetImageWorldBounds
title: ID2D1DeviceContext::GetImageWorldBounds
author: windows-sdk-content
description: Gets the bounds of an image with the world transform of the context applied.
old-location: direct2d\id2d1devicecontext_getimageworldbounds.htm
tech.root: direct2d
ms.assetid: 939531E1-B641-48EF-B129-AC3AA5226919
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: GetImageWorldBounds, GetImageWorldBounds method [Direct2D], GetImageWorldBounds method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],GetImageWorldBounds method, ID2D1DeviceContext.GetImageWorldBounds, ID2D1DeviceContext::GetImageWorldBounds, d2d1_1/ID2D1DeviceContext::GetImageWorldBounds, direct2d.id2d1devicecontext_getimageworldbounds
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
 - ID2D1DeviceContext.GetImageWorldBounds
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext::GetImageWorldBounds


## -description


Gets the bounds of an image with the world transform of the context applied.


## -parameters




### -param image [in]

Type: <b><a href="https://msdn.microsoft.com/9f7b4546-edbe-4000-a4ce-1a69563ebf9d">ID2D1Image</a>*</b>

The image whose bounds will be calculated.


### -param worldBounds [out]

Type: <b><a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>[1]</b>

When this method returns, contains a pointer to the bounds of the image in device independent pixels (DIPs).


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid parameter was passed to the returning function.</td>
</tr>
</table>
 




## -remarks



The image bounds reflect the current DPI, unit mode, and world transform of the context.  To get bounds which don't include the world transform, use <a href="https://msdn.microsoft.com/6a0f4e36-4490-4df5-a520-e10e524c8337">ID2D1DeviceContext::GetImageLocalBounds</a>.




The returned bounds reflect which pixels would be impacted by calling <a href="https://msdn.microsoft.com/c41d8a79-280a-451e-b07b-f904d07da5c7">DrawImage</a> with the same image and a target offset of (0,0).  They do not reflect the current clip rectangle set on the device context or the extent of the context’s current target image.





## -see-also




<a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>



<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>



<a href="https://msdn.microsoft.com/8292da6b-8232-4ef0-967d-a53d586aa9a9">ID2D1DeviceContext::CreateBitmap</a>



<a href="https://msdn.microsoft.com/6a0f4e36-4490-4df5-a520-e10e524c8337">ID2D1DeviceContext::GetImageLocalBounds</a>



<a href="https://msdn.microsoft.com/9f7b4546-edbe-4000-a4ce-1a69563ebf9d">ID2D1Image</a>
 

 

