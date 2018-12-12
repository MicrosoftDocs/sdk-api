---
UID: NF:d2d1_1.ID2D1DeviceContext.GetTarget
title: ID2D1DeviceContext::GetTarget
author: windows-sdk-content
description: Gets the target currently associated with the device context.
old-location: direct2d\id2d1devicecontext_gettarget.htm
tech.root: direct2d
ms.assetid: a70307db-863a-4c59-a327-fb71a5d58f84
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTarget, GetTarget method [Direct2D], GetTarget method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],GetTarget method, ID2D1DeviceContext.GetTarget, ID2D1DeviceContext::GetTarget, d2d1_1/ID2D1DeviceContext::GetTarget, direct2d.id2d1devicecontext_gettarget
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
 - ID2D1DeviceContext.GetTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext::GetTarget


## -description


Gets the target currently associated with the device context.


## -parameters




### -param image [out, optional]

Type: <b><a href="https://msdn.microsoft.com/9f7b4546-edbe-4000-a4ce-1a69563ebf9d">ID2D1Image</a>**</b>

When this method returns, contains the address of a pointer to the target currently associated with the device context.


## -returns



This method does not return a value.




## -remarks



If a target is not associated with the device context, <i>target</i> will contain <b>NULL</b> when the methods returns.

If the currently selected target is a bitmap rather than a command list, the application can gain access to the initial bitmaps created by using one of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd742726(v=VS.85).aspx">CreateHwndRenderTarget</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd742724(v=VS.85).aspx">CreateDxgiSurfaceRenderTarget</a>
</li>
<li>
<a href="https://msdn.microsoft.com/93141743-c11d-40b4-83c5-07c9066836c7">CreateWicBitmapRenderTarget</a>
</li>
<li>
<a href="https://msdn.microsoft.com/de062068-d2b5-4576-a475-a0e2c9840506">CreateDCRenderTarget</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd742780(v=VS.85).aspx">CreateCompatibleRenderTarget</a>
</li>
</ul>
It is not possible for an application to destroy these bitmaps.  All of these bitmaps are bindable as bitmap targets.  However not all of these bitmaps can be used as bitmap sources for  <a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a> methods.


<a href="https://msdn.microsoft.com/en-us/library/Dd742724(v=VS.85).aspx">CreateDxgiSurfaceRenderTarget</a> will create a bitmap that is usable as a bitmap source if the DXGI surface is bindable as a shader resource view.


<a href="https://msdn.microsoft.com/en-us/library/Dd742780(v=VS.85).aspx">CreateCompatibleRenderTarget</a> will always create bitmaps that are usable as a bitmap source.


<a href="https://msdn.microsoft.com/0562b286-7427-4d76-b699-a39356496a0f">ID2D1RenderTarget::BeginDraw</a> will copy from the HDC to the original bitmap associated with it.  <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">ID2D1RenderTarget::EndDraw</a> will copy from the original bitmap to the HDC.  


<a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a> objects will be locked in the following circumstances:

<ul>
<li>BeginDraw has been called and the currently selected target bitmap is a WIC bitmap.</li>
<li>A WIC bitmap is set as the target of a device context after BeginDraw has been called and before EndDraw has been called.</li>
<li>Any of the ID2D1Bitmap::Copy* methods are called with a WIC bitmap as either the source or destination.</li>
</ul>
IWICBitmap objects will be unlocked in the following circumstances:

<ul>
<li>EndDraw is called and the currently selected target bitmap is a WIC bitmap.</li>
<li>A WIC bitmap is removed as the target of a device context between the calls to BeginDraw and EndDraw.</li>
<li>Any of the ID2D1Bitmap::Copy* methods are called with a WIC bitmap as either the source or destination.</li>
</ul>
Direct2D will only lock bitmaps that are not currently locked.

Calling <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> for <a href="https://msdn.microsoft.com/cb992ddd-21b2-4eba-b7c4-e391bdd23a9d">ID2D1GdiInteropRenderTarget</a> will always succeed.  <a href="https://msdn.microsoft.com/40797258-84a0-44ee-8b64-04ceb3eb1998">ID2D1GdiInteropRenderTarget::GetDC</a> will return a device context corresponding to the currently bound target bitmap.  GetDC will fail if the target bitmap was not created with the GDI_COMPATIBLE flag set.


<a href="https://msdn.microsoft.com/en-us/library/Dd742774(v=VS.85).aspx">ID2D1HwndRenderTarget::Resize</a> will return <b>DXGI_ERROR_INVALID_CALL</b> if there are any outstanding references to the original target bitmap associated with the render target.

Although the target can be a command list, it cannot be any other type of image. It cannot be the output image of an effect.




## -see-also




<a href="https://msdn.microsoft.com/669a9377-248c-4a86-b447-ed117fff43a6">ID2D1Bitmap1</a>



<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>



<a href="https://msdn.microsoft.com/8292da6b-8232-4ef0-967d-a53d586aa9a9">ID2D1DeviceContext::CreateBitmap</a>



<a href="https://msdn.microsoft.com/66914048-7bef-4551-bb14-5ab67c727dc5">ID2D1DeviceContext::SetTarget</a>
 

 

