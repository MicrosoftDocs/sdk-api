---
UID: NF:d2d1_1.ID2D1DeviceContext.SetTarget
title: ID2D1DeviceContext::SetTarget (d2d1_1.h)
author: windows-sdk-content
description: The bitmap or command list to which the Direct2D device context will now render.
old-location: direct2d\id2d1devicecontext_settarget.htm
tech.root: Direct2D
ms.assetid: 66914048-7bef-4551-bb14-5ab67c727dc5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID2D1DeviceContext interface [Direct2D],SetTarget method, ID2D1DeviceContext.SetTarget, ID2D1DeviceContext::SetTarget, SetTarget, SetTarget method [Direct2D], SetTarget method [Direct2D],ID2D1DeviceContext interface, d2d1_1/ID2D1DeviceContext::SetTarget, direct2d.id2d1devicecontext_settarget
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
 - ID2D1DeviceContext.SetTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext::SetTarget


## -description


The bitmap or command list to which the <a href="https://msdn.microsoft.com/03b3b91c-9751-4f8d-af24-85067f06930b">Direct2D</a> device context will now render.


## -parameters




### -param image [in, optional]

Type: <b><a href="https://msdn.microsoft.com/9f7b4546-edbe-4000-a4ce-1a69563ebf9d">ID2D1Image</a>*</b>

The surface or command list to which the Direct2D device context will render.


## -returns



This method does not return a value.




## -remarks



The target can be changed at any time, including while the context is drawing.

The target can be either a bitmap created with the <a href="https://msdn.microsoft.com/c080e23e-99c4-46ed-8b21-be26dec288af">D2D1_BITMAP_OPTIONS_TARGET</a> flag, or it can be a command list. Other kinds of images cannot be set as a target. For example, you cannot set the output of an effect as target. If the target is not valid the context will enter the <b>D2DERR_INVALID_TARGET </b>error state.

You cannot  use <b>SetTarget</b> to render to a bitmap/command list from multiple device contexts simultaneously. An image is considered “being rendered to” if it has ever been set on a device context within a <a href="https://msdn.microsoft.com/0562b286-7427-4d76-b699-a39356496a0f">BeginDraw</a>/<a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a> timespan. If an attempt is made to render to an image through multiple device contexts, all subsequent device contexts after the first will enter an error state.



Callers wishing to attach an image to a second device context should first call <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a> on the first device context.


Here is an example of the correct calling order.


```cpp
pDC1->BeginDraw();
pDC1->SetTarget(pImage);
// …
pDC1->EndDraw();

pDC2->BeginDraw();
pDC2->SetTarget(pImage);
// …
pDC2->EndDraw();

```


Here is an example of the incorrect calling order.


```cpp
pDC1->BeginDraw();
pDC2->BeginDraw();

pDC1->SetTarget(pImage);

// ...

pDC1->SetTarget(NULL);

pDC2->SetTarget(pImage); // This call is invalid, even though pImage is no longer set on pDC1.

// ...

pDC1->EndDraw(); // This EndDraw SUCCEEDs.
pDC2->EndDraw(); // This EndDraw FAILs


```


<div class="alert"><b>Note</b>  Changing the target does not change the bitmap that an HWND render target presents from, nor does it change the bitmap that a DC render target blts to/from.</div>
<div> </div>
This API makes it easy for an application to use a bitmap as a source (like in <a href="https://msdn.microsoft.com/95F73EBD-989E-4FB1-B1D2-86642E99FA3E">DrawBitmap</a>) and as a destination at the same time.  Attempting to use a bitmap as a source on the same device context to which it is bound as a target will put the device context into the D2DERR_BITMAP_BOUND_AS_TARGET error state.

It is acceptable to have a bitmap bound as a target bitmap on multiple render targets at once.  Applications that do this must properly synchronize rendering with <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">Flush</a> or <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a>.

You can change the target at any time, including while the context is drawing.

You can set the target to NULL, in which case drawing calls will put the device context into an error state with D2DERR_WRONG_STATE.  Calling <b>SetTarget</b> with a NULL target does not restore the original target bitmap to the device context.

If the device context has an outstanding HDC, the context will enter the <b>D2DERR_WRONG_STATE</b> error state.  The target will not be changed.

If the bitmap and the device context are not in the same resource domain, the context will enter <b>\</b> error state.  The target will not be changed.


<a href="https://msdn.microsoft.com/d0d736b5-0427-4c0d-8085-8498fd00f6b6">ID2D1RenderTarget::GetPixelSize</a> returns the size of the current target bitmap (or 0, 0) if there is no bitmap bound).
<a href="https://msdn.microsoft.com/a46ec1c6-b0ff-4822-ab92-0b0a2ab564ba">ID2D1RenderTarget::GetSize</a> returns the pixel size of the current bitmap scaled by the DPI of the render target.
<b>SetTarget</b> does not affect the DPI of the render target.



<a href="https://msdn.microsoft.com/2dcd9af4-78d7-4271-9113-a91b4bb8145e">ID2D1RenderTarget::GetPixelFormat</a> returns the pixel format of the current target bitmap (or <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT_UNKNOWN</a>, <a href="https://msdn.microsoft.com/f1b1e735-2e89-4dc1-9fee-dfb4626ef453">D2D1_ALPHA_MODE_UNKNOWN</a> if there is none).


<a href="https://msdn.microsoft.com/42e25099-016e-4656-a412-72dd0fbac1fd">ID2D1Bitmap::CopyFromRenderTarget</a> copies from the currently bound target bitmap.




## -see-also




<a href="https://msdn.microsoft.com/669a9377-248c-4a86-b447-ed117fff43a6">ID2D1Bitmap1</a>



<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>



<a href="https://msdn.microsoft.com/8292da6b-8232-4ef0-967d-a53d586aa9a9">ID2D1DeviceContext::CreateBitmap</a>



<a href="https://msdn.microsoft.com/a70307db-863a-4c59-a327-fb71a5d58f84">ID2D1DeviceContext::GetTarget</a>
 

 

