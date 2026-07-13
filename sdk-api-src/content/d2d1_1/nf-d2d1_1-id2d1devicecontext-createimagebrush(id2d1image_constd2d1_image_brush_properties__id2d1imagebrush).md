---
UID: NF:d2d1_1.ID2D1DeviceContext.CreateImageBrush(ID2D1Image,constD2D1_IMAGE_BRUSH_PROPERTIES&,ID2D1ImageBrush)
title: ID2D1DeviceContext::CreateImageBrush(ID2D1Image,const D2D1_IMAGE_BRUSH_PROPERTIES &,ID2D1ImageBrush) (d2d1_1.h)
description: Creates an image brush. The input image can be any type of image, including a bitmap, effect, or a command list. (overload 3/3)
helpviewer_keywords: ["CreateImageBrush","CreateImageBrush method [Direct2D]","CreateImageBrush method [Direct2D]","ID2D1DeviceContext interface","ID2D1DeviceContext interface [Direct2D]","CreateImageBrush method","ID2D1DeviceContext.CreateImageBrush","ID2D1DeviceContext.CreateImageBrush(ID2D1Image","const D2D1_IMAGE_BRUSH_PROPERTIES &","ID2D1ImageBrush)","ID2D1DeviceContext::CreateImageBrush","ID2D1DeviceContext::CreateImageBrush(ID2D1Image","const D2D1_IMAGE_BRUSH_PROPERTIES &","ID2D1ImageBrush)","d2d1_1/ID2D1DeviceContext::CreateImageBrush","direct2d.id2d1devicecontext_createimagebrush3"]
old-location: direct2d\id2d1devicecontext_createimagebrush3.htm
tech.root: Direct2D
ms.assetid: 46EBAD74-44F3-4235-A7D2-C3E960AE702F
ms.date: 12/05/2018
ms.keywords: CreateImageBrush, CreateImageBrush method [Direct2D], CreateImageBrush method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],CreateImageBrush method, ID2D1DeviceContext.CreateImageBrush, ID2D1DeviceContext.CreateImageBrush(ID2D1Image,const D2D1_IMAGE_BRUSH_PROPERTIES &,ID2D1ImageBrush), ID2D1DeviceContext::CreateImageBrush, ID2D1DeviceContext::CreateImageBrush(ID2D1Image,const D2D1_IMAGE_BRUSH_PROPERTIES &,ID2D1ImageBrush), d2d1_1/ID2D1DeviceContext::CreateImageBrush, direct2d.id2d1devicecontext_createimagebrush3
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1DeviceContext::CreateImageBrush
 - d2d1_1/ID2D1DeviceContext::CreateImageBrush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DeviceContext.CreateImageBrush
---

# ID2D1DeviceContext::CreateImageBrush(ID2D1Image,const D2D1_IMAGE_BRUSH_PROPERTIES &,ID2D1ImageBrush)


## -description

Creates an image brush. The input image can be any type of image, including a bitmap, effect, or a command list.

## -parameters

### -param image [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a>*</b>

The image to be used as a source for the image brush.

### -param imageBrushProperties [in, ref]

Type: <b>const <a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_image_brush_properties">D2D1_IMAGE_BRUSH_PROPERTIES</a></b>

The properties specific to an image brush.

### -param imageBrush [out]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1imagebrush">ID2D1ImageBrush</a>**</b>

When this method returns, contains the address of a pointer to the  input rectangles.

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
<td>An invalid value was passed to the method.</td>
</tr>
</table>

## -remarks

The image brush can be used to fill an arbitrary geometry, an opacity mask or text.

This sample illustrates drawing a rectangle with an image brush.


```cpp
HRESULT
CreatePatternBrush(
     __in ID2D1DeviceContext *pDeviceContext,
     __deref_out ID2D1ImageBrush **ppImageBrush
     )
{
    HRESULT hr = S_OK;
    ID2D1Image *pOldTarget = NULL;
    pDeviceContext->GetTarget(&pOldTarget);

    ID2D1CommandList *pCommandList = NULL;
    hr = pDeviceContext->CreateCommandList(&pCommandList);
     
    if (SUCCEEDED(hr))
    {   
        pDeviceContext->SetTarget(pCommandList);
        hr = RenderPatternToCommandList(pDeviceContext);
    }

    pDeviceContext->SetTarget(pOldTarget);

    ID2D1ImageBrush *pImageBrush = NULL;

    if (SUCCEEDED(hr))
    {        
         hr = pDeviceContext->CreateImageBrush(
            pCommandList,
            D2D1::ImageBrushProperties(
                D2D1::RectF(198, 298, 370, 470),
                D2D1_EXTEND_MODE_WRAP,
                D2D1_EXTEND_MODE_WRAP,
                D2D1_INTERPOLATION_MODE_LINEAR
                ),
            &pImageBrush
            );
    }
    
    // Fill a rectangle with the image brush.
    if (SUCCEEDED(hr))
    {
        pDeviceContext->FillRectangle(
            D2D1::RectF(0, 0, 100, 100), pImageBrush);
    }

    SafeRelease(&pImageBrush);
    SafeRelease(&pCommandList);
    SafeRelease(&pOldTarget);
    return hr;
}
```

## -see-also

<a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_brush_properties">D2D1_BRUSH_PROPERTIES</a>



<a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_image_brush_properties">D2D1_IMAGE_BRUSH_PROPERTIES</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createcommandlist">ID2D1DeviceContext::CreateCommandList</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect">ID2D1DeviceContext::CreateEffect</a>



<a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry">ID2D1RenderTarget::DrawGeometry</a>



<a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry">ID2D1RenderTarget::FillGeometry</a>
