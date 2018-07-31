---
UID: NF:xpsobjectmodel.IXpsOMPath.GetAccessibilityShortDescription
title: IXpsOMPath::GetAccessibilityShortDescription
author: windows-sdk-content
description: Gets the short textual description of the object's contents.
old-location: xps\ixpsompath_getaccessibilityshortdescription.htm
old-project: printdocs
ms.assetid: 0124d37a-74c1-4f8b-9d91-c12e92cd5e8c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetAccessibilityShortDescription, GetAccessibilityShortDescription method [XPS Documents and Packaging], GetAccessibilityShortDescription method [XPS Documents and Packaging],IXpsOMPath interface, IXpsOMPath interface [XPS Documents and Packaging],GetAccessibilityShortDescription method, IXpsOMPath.GetAccessibilityShortDescription, IXpsOMPath::GetAccessibilityShortDescription, xps.ixpsompath_getaccessibilityshortdescription, xpsobjectmodel/IXpsOMPath::GetAccessibilityShortDescription
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
 - IXpsOMPath.GetAccessibilityShortDescription
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPath::GetAccessibilityShortDescription


## -description


Gets the short textual description of the object's contents. This  description is used by accessibility clients to describe the object.


## -parameters




### -param shortDescription [out, retval]

The short textual description of the object's contents. If this text has not been set, a <b>NULL</b> pointer will be returned.


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



The value that is returned in <i>shortDescription</i> is the value of the <b>AutomationProperties.Name</b> attribute of the <b>Path</b> element in the document markup.



This method allocates the memory used by the string that is returned in <i>shortDescription</i>.  If <i>shortDescription</i> is not <b>NULL</b>, use the <a href="_com_CoTaskMemFree">CoTaskMemFree</a> function  to free the memory.




## -see-also




<a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

