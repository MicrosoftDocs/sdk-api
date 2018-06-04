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

# IWICBitmapEncoder::CreateNewFrame


## -description


Creates a new <a href="https://msdn.microsoft.com/a8de774b-3783-46be-9a21-c9fec2f10ffd">IWICBitmapFrameEncode</a> instance.


## -parameters




### -param ppIFrameEncode [out]

Type: <b><a href="https://msdn.microsoft.com/a8de774b-3783-46be-9a21-c9fec2f10ffd">IWICBitmapFrameEncode</a>**</b>

A pointer that receives a pointer to the new instance of an <a href="https://msdn.microsoft.com/a8de774b-3783-46be-9a21-c9fec2f10ffd">IWICBitmapFrameEncode</a>.


### -param ppIEncoderOptions [in, out]

Type: <b><a href="_inet_IPropertyBag2_Interface_cpp">IPropertyBag2</a>**</b>

Optional. Receives the named properties to use for subsequent frame initialization. See Remarks.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The parameter <i>ppIEncoderOptions</i> can be used to receive an <a href="_inet_IPropertyBag2_Interface_cpp">IPropertyBag2</a> that can then be used to specify encoder options. This is done by passing a pointer to a <b>NULL</b> IPropertyBag2 pointer in <i>ppIEncoderOptions</i>. The returned IPropertyBag2 is initialized with all encoder options that are available for the given format, at their default values. To specify non-default encoding behavior, set the needed encoder options on the IPropertyBag2 and pass it to <a href="https://msdn.microsoft.com/ec215e32-b4bd-469a-903d-f5b546185183">IWICBitmapFrameEncode::Initialize</a>.

<div class="alert"><b>Note</b>  Do not pass in a pointer to an initialized <a href="_inet_IPropertyBag2_Interface_cpp">IPropertyBag2</a>. The pointer will be overwritten, and the original IPropertyBag2 will not be freed.</div>
<div> </div>
Otherwise, you can pass <b>NULL</b> in <i>ppIEncoderOptions</i> if you do not intend to specify encoder options.

See <a href="https://msdn.microsoft.com/e1e3a9d9-209b-46a6-92da-5570476507cf">Encoding Overview</a> for an example of how to set encoder options.

For formats that support encoding multiple frames (for example, TIFF, JPEG-XR), you can work on only one frame at a time. This means that you must call <a href="https://msdn.microsoft.com/6321fb9e-9ea8-423c-a332-9daa589af6f7">IWICBitmapFrameEncode::Commit</a> before you call <b>CreateNewFrame</b> again.





## -see-also




<a href="https://msdn.microsoft.com/e1e3a9d9-209b-46a6-92da-5570476507cf">Encoding Overview</a>



<a href="_inet_IPropertyBag2_Interface_cpp">IPropertyBag2</a>



<a href="https://msdn.microsoft.com/fe87c9ae-dedf-4ec2-ac11-0ea5fc6aa3ad">IWICBitmapEncoder</a>
 

 

