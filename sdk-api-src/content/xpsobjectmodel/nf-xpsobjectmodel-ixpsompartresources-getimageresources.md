---
UID: NF:xpsobjectmodel.IXpsOMPartResources.GetImageResources
title: IXpsOMPartResources::GetImageResources
author: windows-sdk-content
description: Gets the IXpsOMImageResourceCollection interface that contains the images that are used in the XPS document.
old-location: xps\ixpsompartresources_getimageresources.htm
tech.root: printdocs
ms.assetid: d30281b7-0b2c-4240-813b-a53c8acb819c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetImageResources, GetImageResources method [XPS Documents and Packaging], GetImageResources method [XPS Documents and Packaging],IXpsOMPartResources interface, IXpsOMPartResources interface [XPS Documents and Packaging],GetImageResources method, IXpsOMPartResources.GetImageResources, IXpsOMPartResources::GetImageResources, xps.ixpsompartresources_getimageresources, xpsobjectmodel/IXpsOMPartResources::GetImageResources
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
 - IXpsOMPartResources.GetImageResources
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPartResources::GetImageResources


## -description


Gets the  <a href="https://msdn.microsoft.com/aed8b23e-71fd-49e6-aae9-006a59e0111b">IXpsOMImageResourceCollection</a> interface that contains the images that are used in the XPS document.


## -parameters




### -param imageResources [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/aed8b23e-71fd-49e6-aae9-006a59e0111b">IXpsOMImageResourceCollection</a> interface that contains the images that are used in the XPS document.


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
<i>imageResources</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



After loading and parsing the resource into the XPS OM, this method might return an error that applies to another resource. This occurs because all of the relationships are parsed when a resource is loaded.




## -see-also




<a href="https://msdn.microsoft.com/aed8b23e-71fd-49e6-aae9-006a59e0111b">IXpsOMImageResourceCollection</a>



<a href="https://msdn.microsoft.com/9f706f23-25a0-40ee-93f4-3d7ac98ad6ed">IXpsOMPartResources</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

