---
UID: NF:d2d1_1.ID2D1DeviceContext.CreateImageBrush
title: ID2D1DeviceContext::CreateImageBrush (d2d1_1.h)
author: windows-sdk-content
description: Creates an image brush. The input image can be any type of image, including a bitmap, effect, or a command list.
old-location: direct2d\id2d1devicecontext_createimagebrush.htm
tech.root: Direct2D
ms.assetid: f80947b7-7bd9-4097-8279-f70f5d92d5b6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateImageBrush, CreateImageBrush method [Direct2D], CreateImageBrush method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],CreateImageBrush method, ID2D1DeviceContext.CreateImageBrush, ID2D1DeviceContext::CreateImageBrush, ID2D1DeviceContext::CreateImageBrush(ID2D1Image,const D2D1_IMAGE_BRUSH_PROPERTIES,const D2D1_BRUSH_PROPERTIES,ID2D1ImageBrush), d2d1_1/ID2D1DeviceContext::CreateImageBrush, direct2d.id2d1devicecontext_createimagebrush
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
 - ID2D1DeviceContext.CreateImageBrush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext::CreateImageBrush


## -description


Creates an image brush. The input image can be any type of image, including a bitmap, effect, or a command list.



## -parameters




### -param image [in]

Type: <b><a href="https://msdn.microsoft.com/9f7b4546-edbe-4000-a4ce-1a69563ebf9d">ID2D1Image</a>*</b>

The image to be used as a source for the image brush.


### -param imageBrushProperties [in]

Type: <b>const <a href="https://msdn.microsoft.com/c7bcae4d-cdef-4bfc-aa5a-68b85497a7f6">D2D1_IMAGE_BRUSH_PROPERTIES</a>*</b>

The properties specific to an image brush.


### -param brushProperties [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/37b2fc18-a320-41c0-8717-dcd561a2f2df">D2D1_BRUSH_PROPERTIES</a>*</b>

Properties  common to all brushes.


### -param imageBrush [out]

Type: <b><a href="https://msdn.microsoft.com/c5088ce2-5744-4061-957b-25831478a714">ID2D1ImageBrush</a>**</b>

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




<a href="https://msdn.microsoft.com/37b2fc18-a320-41c0-8717-dcd561a2f2df">D2D1_BRUSH_PROPERTIES</a>



<a href="https://msdn.microsoft.com/c7bcae4d-cdef-4bfc-aa5a-68b85497a7f6">D2D1_IMAGE_BRUSH_PROPERTIES</a>



<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>



<a href="https://msdn.microsoft.com/f34710dc-7845-457f-9b27-51ae937d9f74">ID2D1DeviceContext::CreateCommandList</a>



<a href="https://msdn.microsoft.com/dfe587f9-e92f-4367-a503-edd446a91cb8">ID2D1DeviceContext::CreateEffect</a>



<a href="https://msdn.microsoft.com/319b2680-34f8-4e00-985e-47ff87115794">ID2D1RenderTarget::DrawGeometry</a>



<a href="https://msdn.microsoft.com/097f21ac-a062-4ce1-bdc7-87317dbdf5be">ID2D1RenderTarget::FillGeometry</a>
 

 

