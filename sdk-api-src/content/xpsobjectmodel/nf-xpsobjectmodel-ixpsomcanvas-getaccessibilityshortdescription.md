---
UID: NF:xpsobjectmodel.IXpsOMCanvas.GetAccessibilityShortDescription
title: IXpsOMCanvas::GetAccessibilityShortDescription
author: windows-sdk-content
description: Gets a short textual description of the object's contents.
old-location: xps\ixpsomcanvas_getaccessibilityshortdescription.htm
tech.root: printdocs
ms.assetid: c07f394d-b10f-45c1-b8b7-cd466507967b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetAccessibilityShortDescription, GetAccessibilityShortDescription method [XPS Documents and Packaging], GetAccessibilityShortDescription method [XPS Documents and Packaging],IXpsOMCanvas interface, IXpsOMCanvas interface [XPS Documents and Packaging],GetAccessibilityShortDescription method, IXpsOMCanvas.GetAccessibilityShortDescription, IXpsOMCanvas::GetAccessibilityShortDescription, xps.ixpsomcanvas_getaccessibilityshortdescription, xpsobjectmodel/IXpsOMCanvas::GetAccessibilityShortDescription
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
 - IXpsOMCanvas.GetAccessibilityShortDescription
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
- IXpsOMCanvas.GetAccessibilityShortDescription
: 
---

# IXpsOMCanvas::GetAccessibilityShortDescription


## -description


Gets a short textual description of the object's contents. This  text is used by accessibility clients to describe the object.


## -parameters




### -param shortDescription [out, retval]

The short textual description of the object's contents. If this description is not set, a <b>NULL</b> pointer is returned.


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
<i>shortDescription</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The property returned by this method corresponds to the <b>AutomationProperties.Name</b> attribute of the <b>Canvas</b> element in the document markup.

This method allocates the memory used by the string that is returned in <i>shortDescription</i>.  If <i>shortDescription</i> is not <b>NULL</b>, use the <b>CoTaskMemFree</b> function to free the memory.




## -see-also




<a href="https://msdn.microsoft.com/3cb0e1b3-88a8-4724-a3c5-0df416294e62">IXpsOMCanvas</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

