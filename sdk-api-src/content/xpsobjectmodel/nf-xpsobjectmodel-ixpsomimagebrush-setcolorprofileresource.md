---
UID: NF:xpsobjectmodel.IXpsOMImageBrush.SetColorProfileResource
title: IXpsOMImageBrush::SetColorProfileResource
author: windows-sdk-content
description: Sets a pointer to the IXpsOMColorProfileResource interface, which contains the color profile resource that is associated with the image.
old-location: xps\ixpsomimagebrush_setcolorprofileresource.htm
tech.root: printdocs
ms.assetid: d18511b7-13ed-4528-9f3d-aef3bcadc403
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXpsOMImageBrush interface [XPS Documents and Packaging],SetColorProfileResource method, IXpsOMImageBrush.SetColorProfileResource, IXpsOMImageBrush::SetColorProfileResource, SetColorProfileResource, SetColorProfileResource method [XPS Documents and Packaging], SetColorProfileResource method [XPS Documents and Packaging],IXpsOMImageBrush interface, xps.ixpsomimagebrush_setcolorprofileresource, xpsobjectmodel/IXpsOMImageBrush::SetColorProfileResource
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
 - IXpsOMImageBrush.SetColorProfileResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMImageBrush::SetColorProfileResource


## -description


Sets a pointer to the <a href="https://msdn.microsoft.com/8a344300-c3fc-4225-bfa5-d5d33798a094">IXpsOMColorProfileResource</a> interface, which contains the color profile resource that is associated with the image.


## -parameters




### -param colorProfileResource [in]

The color profile resource that is associated with the image. A <b>NULL</b> pointer will release any previously set color profile resources.


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
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>colorProfileResource</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8a344300-c3fc-4225-bfa5-d5d33798a094">IXpsOMColorProfileResource</a>



<a href="https://msdn.microsoft.com/f5478582-466b-496e-b7f3-42fb8caa6814">IXpsOMImageBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

