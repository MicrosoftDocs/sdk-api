---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# MFCreateDXSurfaceBuffer function


## -description



          Creates a media buffer object that manages a Direct3D 9 surface.
        


## -parameters




### -param riid [in]


            Identifies the type of Direct3D 9 surface. Currently this value must be <b>IID_IDirect3DSurface9</b>.
          


### -param punkSurface [in]


            A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of the DirectX surface.
          


### -param fBottomUpWhenLinear [in]


            If <b>TRUE</b>, the buffer's <a href="https://msdn.microsoft.com/32601f2e-ab91-4a65-bcf4-8e063e90fbb0">IMF2DBuffer::ContiguousCopyTo</a> method copies the buffer into a bottom-up format. The bottom-up format is compatible with GDI for uncompressed RGB images. If this parameter is <b>FALSE</b>, the <b>ContiguousCopyTo</b> method copies the buffer into a top-down format, which is compatible with DirectX.
          

For more information about top-down versus bottom-up images, see <a href="https://msdn.microsoft.com/13cd1106-48b3-4522-ac09-8efbaab5c31d">Image Stride</a>.


### -param ppBuffer [out]


            Receives a pointer to the <a href="https://msdn.microsoft.com/3ccc7089-d0d0-4eb1-b763-0d4e348af685">IMFMediaBuffer</a> interface. The caller must release the buffer.
          


## -returns




            The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">

                The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
</table>
 




## -remarks



This function creates a media buffer object that holds a pointer to the Direct3D surface specified in <i>punkSurface</i>. Locking the buffer gives the caller access to the surface memory. When the buffer object is destroyed, it releases the surface. For more information about media buffers, see <a href="https://msdn.microsoft.com/3ee073ea-7bac-4971-9167-93a4e541ab77">Media Buffers</a>.

<div class="alert"><b>Note</b>  This function does not allocate the Direct3D surface itself.</div>
<div> </div>

        The buffer object created by this function also exposes the <a href="https://msdn.microsoft.com/80eb23db-a7c0-4dbe-97d8-0dc07a34d8f7">IMF2DBuffer</a> interface. For more information, see <a href="https://msdn.microsoft.com/2c82c023-4436-4f8a-b896-7f4765f989b3">DirectX Surface Buffer</a>.
      

This function does not support DXGI surfaces.




## -see-also




<a href="https://msdn.microsoft.com/2c82c023-4436-4f8a-b896-7f4765f989b3">DirectX Surface Buffer</a>



<a href="https://msdn.microsoft.com/3ee073ea-7bac-4971-9167-93a4e541ab77">Media Buffers</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

