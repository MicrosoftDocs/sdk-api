---
UID: NF:xpsobjectmodel.IXpsOMPageReference.SetThumbnailResource
title: IXpsOMPageReference::SetThumbnailResource
author: windows-sdk-content
description: Sets the pointer to the IXpsOMImageResource interface of the thumbnail image resource to be assigned to the page.
old-location: xps\ixpsompagereference_setthumbnailresource.htm
tech.root: printdocs
ms.assetid: b44c041d-dccd-4b64-b85b-454b203b865b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IXpsOMPageReference interface [XPS Documents and Packaging],SetThumbnailResource method, IXpsOMPageReference.SetThumbnailResource, IXpsOMPageReference::SetThumbnailResource, SetThumbnailResource, SetThumbnailResource method [XPS Documents and Packaging], SetThumbnailResource method [XPS Documents and Packaging],IXpsOMPageReference interface, xps.ixpsompagereference_setthumbnailresource, xpsobjectmodel/IXpsOMPageReference::SetThumbnailResource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMPageReference.SetThumbnailResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xpsobjectmodel.h
: 
- IXpsOMPageReference.SetThumbnailResource
: 
---

# IXpsOMPageReference::SetThumbnailResource


## -description


Sets the pointer to the <a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a> interface of the thumbnail image resource to be assigned to the page.


## -parameters




### -param imageResource [in]

A pointer to the <a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a> interface  of the thumbnail image resource to be assigned to the page. If an <b>IXpsOMImageResource</b> interface has been set, a <b>NULL</b> pointer will release it.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

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
<dt><b>XPS_E_INVALID_THUMBNAIL_IMAGE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The image in  <i>imageResource</i> is not a supported image type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>imageResource</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>
 




## -remarks



The thumbnail image is a small, visual representation of the document's   contents.

The image type of the image resource must be either  <a href="https://msdn.microsoft.com/b4300a8c-f0bf-465f-a717-c54de95c1183">XPS_IMAGE_TYPE_JPEG</a> or <b>XPS_IMAGE_TYPE_PNG</b>.




## -see-also




<a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a>



<a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a>



<a href="https://msdn.microsoft.com/cac794c0-bea2-417e-880f-15838f718ba7">IXpsOMThumbnailGenerator</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/b4300a8c-f0bf-465f-a717-c54de95c1183">XPS_IMAGE_TYPE</a>
 

 

