---
UID: NF:xpsobjectmodel.IXpsOMThumbnailGenerator.GenerateThumbnail
title: IXpsOMThumbnailGenerator::GenerateThumbnail
author: windows-sdk-content
description: Generates a thumbnail image of a page.
old-location: xps\ixpsomthumbnailgenerator_generatethumbnail.htm
old-project: printdocs
ms.assetid: 8a2431f0-50e5-43a9-8940-62d9babad297
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: GenerateThumbnail, GenerateThumbnail method [XPS Documents and Packaging], GenerateThumbnail method [XPS Documents and Packaging],IXpsOMThumbnailGenerator interface, IXpsOMThumbnailGenerator interface [XPS Documents and Packaging],GenerateThumbnail method, IXpsOMThumbnailGenerator.GenerateThumbnail, IXpsOMThumbnailGenerator::GenerateThumbnail, xps.ixpsomthumbnailgenerator_generatethumbnail, xpsobjectmodel/IXpsOMThumbnailGenerator::GenerateThumbnail
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: XPS_INTERLEAVING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMThumbnailGenerator.GenerateThumbnail
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMThumbnailGenerator::GenerateThumbnail


## -description


Generates a thumbnail image of a page.


## -parameters




### -param page [in]

A pointer to the <a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a> interface that contains the page for which the thumbnail image will be created.


### -param thumbnailType [in]

The <a href="https://msdn.microsoft.com/b4300a8c-f0bf-465f-a717-c54de95c1183">XPS_IMAGE_TYPE</a> value that specifies the type of thumbnail image to create.


### -param thumbnailSize [in]

The <a href="https://msdn.microsoft.com/308083dd-74b4-4674-b5d7-e14e917fbc1f">XPS_THUMBNAIL_SIZE</a> value that specifies the image size of the thumbnail to create.


### -param imageResourcePartName [in]

A pointer to the <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface that contains the name of the new thumbnail image part.


### -param imageResource [out, retval]

A pointer to the new <a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a> interface that contains the thumbnail image created by this method.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>page</i>, <i>imageResourcePartName</i>, or <i>imageResource</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the following parameters contains a value that is not valid:

<ul>
<li><i>thumbnailType</i>: The image type must be PNG (<a href="https://msdn.microsoft.com/b4300a8c-f0bf-465f-a717-c54de95c1183">XPS_IMAGE_TYPE_PNG</a>) or JPEG (<b>XPS_IMAGE_TYPE_JPEG</b>)</li>
<li><i>thumbnailSize</i>: <i>thumbnailSize</i> must be a member of  <a href="https://msdn.microsoft.com/308083dd-74b4-4674-b5d7-e14e917fbc1f">XPS_THUMBNAIL_SIZE</a>
</li>
</ul>
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a>



<a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a>



<a href="https://msdn.microsoft.com/cac794c0-bea2-417e-880f-15838f718ba7">IXpsOMThumbnailGenerator</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/b4300a8c-f0bf-465f-a717-c54de95c1183">XPS_IMAGE_TYPE</a>



<a href="https://msdn.microsoft.com/308083dd-74b4-4674-b5d7-e14e917fbc1f">XPS_THUMBNAIL_SIZE</a>
 

 

