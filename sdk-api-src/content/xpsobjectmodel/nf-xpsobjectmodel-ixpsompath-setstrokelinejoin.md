---
UID: NF:xpsobjectmodel.IXpsOMPath.SetStrokeLineJoin
title: IXpsOMPath::SetStrokeLineJoin
author: windows-sdk-content
description: Sets the style for joining stroke lines.
old-location: xps\ixpsompath_setstrokelinejoin.htm
old-project: printdocs
ms.assetid: cd650051-ee26-4a8a-b344-2fe84fb2c2a5
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IXpsOMPath interface [XPS Documents and Packaging],SetStrokeLineJoin method, IXpsOMPath.SetStrokeLineJoin, IXpsOMPath::SetStrokeLineJoin, SetStrokeLineJoin, SetStrokeLineJoin method [XPS Documents and Packaging], SetStrokeLineJoin method [XPS Documents and Packaging],IXpsOMPath interface, xps.ixpsompath_setstrokelinejoin, xpsobjectmodel/IXpsOMPath::SetStrokeLineJoin
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
req.typenames: XPS_INTERLEAVING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMPath.SetStrokeLineJoin
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPath::SetStrokeLineJoin


## -description


Sets the  style for joining stroke lines.


## -parameters




### -param strokeLineJoin [in]

The <a href="https://msdn.microsoft.com/b0409564-a6b3-4e9d-b136-3d865dd46f1d">XPS_LINE_JOIN</a> value to be set.


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
<dt><b>E_INVALIDARG </b></dt>
</dl>
</td>
<td width="60%">
<i>strokeLineJoin</i> is not a valid <a href="https://msdn.microsoft.com/b0409564-a6b3-4e9d-b136-3d865dd46f1d">XPS_LINE_JOIN</a> value.

</td>
</tr>
</table>
 




## -remarks



For more information about the line join styles, see <a href="https://msdn.microsoft.com/b0409564-a6b3-4e9d-b136-3d865dd46f1d">XPS_LINE_JOIN</a>.




## -see-also




<a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

