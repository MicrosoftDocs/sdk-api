---
UID: NF:dcomp.IDCompositionSurface.BeginDraw
title: IDCompositionSurface::BeginDraw
author: windows-sdk-content
description: Initiates drawing on this Microsoft DirectComposition surface object.
old-location: directcomp\idcompositionsurface_begindraw.htm
tech.root: directcomp
ms.assetid: 0D7E90A1-90E4-44BE-A4DA-8DA300C81A35
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: BeginDraw, BeginDraw method [DirectComposition], BeginDraw method [DirectComposition],IDCompositionSurface interface, IDCompositionSurface interface [DirectComposition],BeginDraw method, IDCompositionSurface.BeginDraw, IDCompositionSurface::BeginDraw, dcomp/IDCompositionSurface::BeginDraw, directcomp.idcompositionsurface_begindraw
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionSurface.BeginDraw
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionSurface::BeginDraw


## -description


Initiates drawing on this Microsoft DirectComposition surface object. The update rectangle must be within the boundaries of the surface; otherwise, this method fails.




## -parameters




### -param updateRect [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

The rectangle to be updated. If this parameter is NULL, the entire bitmap is updated.


### -param iid [in]

Type: <b>REFIID</b>

The identifier of the interface to retrieve.


### -param updateObject

TBD


### -param updateOffset [out]

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>*</b>

The offset into the surface where the application should draw updated content. This offset will reference the upper left corner of the update rectangle.


#### - upateObject [out]

Type: <b>void**</b>

Receives an interface pointer of the type specified in the <i>iid</i> parameter.   This parameter must not be NULL.

<div class="alert"><b>Note</b>  In Windows 8, this parameter was <i>surface</i>.</div>
<div> </div>

## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. 




## -remarks



This method enables an application to incrementally update the contents of a DirectComposition surface object. The application must use the following sequence:



<ol>
<li>Call <b>BeginDraw</b> to initiate the incremental update.</li>
<li>Use the retrieved surface as a render target and draw the updated contents at the retrieved offset.</li>
<li>Call the <a href="https://msdn.microsoft.com/127195F7-6000-4D8C-B850-3E4D40BC4082">IDCompositionSurface::EndDraw</a> method to finish the update.</li>
</ol>
The update object returned by this method is either a Direct2D device context or a DXGI surface, depending on the value of the <i>iid</i> parameter and on how the DirectComposition surface object was created. If the <i>iid</i> parameter is __uuidof(ID2D1DeviceContext), then the returned object is a Direct2D device context that already has the DirectComposition surface selected as a render target. Otherwise, it is a DXGI surface which the application may use as a render target. In either case, the returned object is associated with the Direct2D or DXGI device passed by the application to the DCompositionCreateDevice2 function or the <a href="https://msdn.microsoft.com/20E60EAE-68CB-45B8-BC50-3D12F449AA6E">IDCompositionDevice2::CreateSurfaceFactory</a> method.



The <i>iid</i> parameter may only be __uuidof(ID2D1DeviceContext) if the DirectComposition surface object was created from a DirectComposition device or surface factory that was, itself, created with an associated Direct2D device. In particular, the application must have called either the DCompositionCreateDevice2 function or the <a href="https://msdn.microsoft.com/20E60EAE-68CB-45B8-BC50-3D12F449AA6E">IDCompositionDevice2::CreateSurfaceFactory</a> method with a Direct2D device as the <i>renderingDevice</i> parameter. If the DirectComposition surface was created via a surface factory that was not associated with a Direct2D device, or if it was created directly via the IDCompositionDevice2 interface and the device was not directly associated with a Direct2D device, then passing __uuidof(ID2D1DeviceContext) as the iid parameter causes this method to return E_INVALIDARG.



If the application successfully retrieves a Direct2D device context as the update object, then the application should not call either the ID2D1DeviceContext::BeginDraw or ID2D1DeviceContext::EndDraw methods on the returned Direct2D device context.


The retrieved offset is not necessarily the same as the top-left corner of the requested update rectangle. The application must transform its rendering primitives to draw within a rectangle of the same width and height as the input rectangle, but at the given offset. The application should not draw outside of this rectangle.



If the <i>updateRectangle</i> parameter is NULL, the entire surface is updated. In that case, because the retrieved offset still might not be (0,0), the application still needs to transform its rendering primitives accordingly.



If the surface is not a virtual surface, then the first time the application calls this method for a particular non-virtual surface, the update rectangle must cover the entire surface, either by specifying the full surface in the requested update rectangle, or by specifying NULL as the <i>updateRectangle</i> parameter. For virtual surfaces, the first call may be any sub-rectangle of the surface.



Because each call to this method might retrieve a different object in the <i>updateObject</i> surface, the application should not cache the retrieved surface pointer. The application should release the retrieved pointer as soon as it finishes drawing. 

The retrieved surface rectangle does not contain the previous contents of the bitmap. The application must update every pixel in the update rectangle, either by first clearing the render target, or by issuing enough rendering primitives to fully cover the update rectangle. Because the initial contents of the update surface are undefined, failing to update every pixel leads to undefined behavior.



Only one DirectComposition surface can be updated at a time. An application must suspend drawing on one surface before beginning or resuming to draw on another surface. If the application calls <b>BeginDraw</b> twice, either for the same surface or for another surface belonging to the same DirectComposition device, without an intervening call to <a href="https://msdn.microsoft.com/127195F7-6000-4D8C-B850-3E4D40BC4082">IDCompositionSurface::EndDraw</a>, the second call fails. If the application calls <a href="https://msdn.microsoft.com/8C24DE03-CF1E-4DC4-8C27-913DAD278579">IDCompositionDevice2::Commit</a> without calling <b>EndDraw</b>, the update remains pending. The update takes effect only after the application calls <b>EndDraw</b> and then  calls the <b>IDCompositionDevice2::Commit</b>  method.




## -see-also




<a href="https://msdn.microsoft.com/E271B4DC-5F09-426A-A5D3-43A48F30CB24">IDCompositionSurface</a>



<a href="https://msdn.microsoft.com/127195F7-6000-4D8C-B850-3E4D40BC4082">IDCompositionSurface::EndDraw</a>
 

 

