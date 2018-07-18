---
UID: NF:xpsobjectmodel.IXpsOMGeometry.SetFillRule
title: IXpsOMGeometry::SetFillRule
author: windows-sdk-content
description: Sets the XPS_FILL_RULE value that describes the fill rule to be used.
old-location: xps\ixpsomgeometry_setfillrule.htm
old-project: printdocs
ms.assetid: e219a505-48e0-46b0-a739-d46fb898bc58
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IXpsOMGeometry interface [XPS Documents and Packaging],SetFillRule method, IXpsOMGeometry.SetFillRule, IXpsOMGeometry::SetFillRule, SetFillRule, SetFillRule method [XPS Documents and Packaging], SetFillRule method [XPS Documents and Packaging],IXpsOMGeometry interface, xps.ixpsomgeometry_setfillrule, xpsobjectmodel/IXpsOMGeometry::SetFillRule
ms.prod: windows
ms.technology: windows-sdk
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
 - IXpsOMGeometry.SetFillRule
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGeometry::SetFillRule


## -description


Sets the  <a href="https://msdn.microsoft.com/353a4dc3-0c4d-46df-ae31-cc94c4116ca3">XPS_FILL_RULE</a> value that describes the fill rule to be used.


## -parameters




### -param fillRule [in]

The <a href="https://msdn.microsoft.com/353a4dc3-0c4d-46df-ae31-cc94c4116ca3">XPS_FILL_RULE</a> value that describes the fill rule to be used.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>fillRule</i> is not a valid <a href="https://msdn.microsoft.com/353a4dc3-0c4d-46df-ae31-cc94c4116ca3">XPS_FILL_RULE</a> value.

</td>
</tr>
</table>
 




## -remarks



For more information about how the file rule determines whether a point is inside the fill region, see <a href="https://msdn.microsoft.com/353a4dc3-0c4d-46df-ae31-cc94c4116ca3">XPS_FILL_RULE</a>. 

In the document markup, this value corresponds to the <b>FillRule</b> attribute of the <b>PathGeometry</b> element.




## -see-also




<a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/353a4dc3-0c4d-46df-ae31-cc94c4116ca3">XPS_FILL_RULE</a>
 

 

