---
UID: NF:xpsobjectmodel.IXpsOMImageBrush.GetImageResource
title: IXpsOMImageBrush::GetImageResource
author: windows-sdk-content
description: Gets a pointer to the IXpsOMImageResource interface, which contains the image resource to be used as the source for the brush.
old-location: xps\ixpsomimagebrush_getimageresource.htm
old-project: printdocs
ms.assetid: 92b03d98-22ce-4856-afe1-d13fb74eb340
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: GetImageResource, GetImageResource method [XPS Documents and Packaging], GetImageResource method [XPS Documents and Packaging],IXpsOMImageBrush interface, IXpsOMImageBrush interface [XPS Documents and Packaging],GetImageResource method, IXpsOMImageBrush.GetImageResource, IXpsOMImageBrush::GetImageResource, xps.ixpsomimagebrush_getimageresource, xpsobjectmodel/IXpsOMImageBrush::GetImageResource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMImageBrush.GetImageResource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMImageBrush::GetImageResource


## -description


Gets a pointer to the <a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a> interface, which contains the image resource to be used as the source for the brush.


## -parameters




### -param imageResource [out, retval]

A pointer to the  <a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a> interface that contains the image resource to be used as the source for the brush.


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
<i>imageResource</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



After loading and parsing the resource into the XPS OM, this method might return an error that applies to another resource. This occurs because all of the relationships are parsed when a resource is loaded.




## -see-also




<a href="https://msdn.microsoft.com/f5478582-466b-496e-b7f3-42fb8caa6814">IXpsOMImageBrush</a>



<a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

