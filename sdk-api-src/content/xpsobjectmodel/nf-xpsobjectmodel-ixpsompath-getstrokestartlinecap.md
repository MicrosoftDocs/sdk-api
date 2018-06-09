---
UID: NF:xpsobjectmodel.IXpsOMPath.GetStrokeStartLineCap
title: IXpsOMPath::GetStrokeStartLineCap
author: windows-sdk-content
description: Gets the style of the line cap at the start of the stroke line.
old-location: xps\ixpsompath_getstrokestartlinecap.htm
old-project: printdocs
ms.assetid: 66286aca-3b94-4ded-9180-1e07599986db
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetStrokeStartLineCap, GetStrokeStartLineCap method [XPS Documents and Packaging], GetStrokeStartLineCap method [XPS Documents and Packaging],IXpsOMPath interface, IXpsOMPath interface [XPS Documents and Packaging],GetStrokeStartLineCap method, IXpsOMPath.GetStrokeStartLineCap, IXpsOMPath::GetStrokeStartLineCap, xps.ixpsompath_getstrokestartlinecap, xpsobjectmodel/IXpsOMPath::GetStrokeStartLineCap
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMPath.GetStrokeStartLineCap
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPath::GetStrokeStartLineCap


## -description


Gets the style of the  line cap at the start of the stroke line.


## -parameters




### -param strokeStartLineCap [out, retval]

The <a href="https://msdn.microsoft.com/63ee8c2d-e7c5-4453-9555-25896dc13870">XPS_LINE_CAP</a> value that indicates the style of the  line cap at the start of the stroke line.


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
<i>strokeStartLineCap</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



For more information about the shapes of line caps, see <a href="https://msdn.microsoft.com/63ee8c2d-e7c5-4453-9555-25896dc13870">XPS_LINE_CAP</a>.




## -see-also




<a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/63ee8c2d-e7c5-4453-9555-25896dc13870">XPS_LINE_CAP</a>
 

 

