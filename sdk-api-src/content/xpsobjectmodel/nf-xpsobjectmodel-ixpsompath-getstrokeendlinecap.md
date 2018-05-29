---
UID: NF:xpsobjectmodel.IXpsOMPath.GetStrokeEndLineCap
title: IXpsOMPath::GetStrokeEndLineCap
author: windows-sdk-content
description: Gets the style of the stroke line's end cap.
old-location: xps\ixpsompath_getstrokeendlinecap.htm
old-project: printdocs
ms.assetid: 54b4f6e7-3a76-48d3-a180-2bb3a532fc67
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: GetStrokeEndLineCap, GetStrokeEndLineCap method [XPS Documents and Packaging], GetStrokeEndLineCap method [XPS Documents and Packaging],IXpsOMPath interface, IXpsOMPath interface [XPS Documents and Packaging],GetStrokeEndLineCap method, IXpsOMPath.GetStrokeEndLineCap, IXpsOMPath::GetStrokeEndLineCap, xps.ixpsompath_getstrokeendlinecap, xpsobjectmodel/IXpsOMPath::GetStrokeEndLineCap
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
-	IXpsOMPath.GetStrokeEndLineCap
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPath::GetStrokeEndLineCap


## -description


Gets the style of the stroke line's  end cap.


## -parameters




### -param strokeEndLineCap [out, retval]

The <a href="https://msdn.microsoft.com/63ee8c2d-e7c5-4453-9555-25896dc13870">XPS_LINE_CAP</a> value that specifies the style of the stroke line's end cap.


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
<i>strokeEndLineCap</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



For more information about line   end cap styles, see <a href="https://msdn.microsoft.com/63ee8c2d-e7c5-4453-9555-25896dc13870">XPS_LINE_CAP</a>.




## -see-also




<a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/63ee8c2d-e7c5-4453-9555-25896dc13870">XPS_LINE_CAP</a>
 

 

