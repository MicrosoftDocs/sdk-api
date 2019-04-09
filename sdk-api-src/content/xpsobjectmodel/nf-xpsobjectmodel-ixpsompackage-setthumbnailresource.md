---
UID: NF:xpsobjectmodel.IXpsOMPackage.SetThumbnailResource
title: IXpsOMPackage::SetThumbnailResource (xpsobjectmodel.h)
author: windows-sdk-content
description: Sets the thumbnail image of the XPS document.
old-location: xps\ixpsompackage_setthumbnailresource.htm
tech.root: printdocs
ms.assetid: 1d5d5332-f6e1-4fad-8b45-c518196c17d2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsOMPackage interface [XPS Documents and Packaging],SetThumbnailResource method, IXpsOMPackage.SetThumbnailResource, IXpsOMPackage::SetThumbnailResource, SetThumbnailResource, SetThumbnailResource method [XPS Documents and Packaging], SetThumbnailResource method [XPS Documents and Packaging],IXpsOMPackage interface, xps.ixpsompackage_setthumbnailresource, xpsobjectmodel/IXpsOMPackage::SetThumbnailResource
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
 - IXpsOMPackage.SetThumbnailResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPackage::SetThumbnailResource


## -description


Sets the thumbnail image of the XPS document.


## -parameters




### -param imageResource [in]

The <a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a> interface that contains the thumbnail image that will be assigned to the package. A <b>NULL</b> pointer releases any previously assigned thumbnail image resources.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.

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

The image type of the image resource must be either  <a href="https://msdn.microsoft.com/en-us/library/Dd372960(v=VS.85).aspx">XPS_IMAGE_TYPE_JPEG</a> or <b>XPS_IMAGE_TYPE_PNG</b>.




## -see-also




<a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a>



<a href="https://msdn.microsoft.com/7b0a36d6-1af1-4c2c-af14-d6139e9115c3">IXpsOMPackage</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd372960(v=VS.85).aspx">XPS_IMAGE_TYPE</a>
 

 

