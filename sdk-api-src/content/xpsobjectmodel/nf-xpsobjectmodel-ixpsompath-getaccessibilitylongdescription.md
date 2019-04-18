---
UID: NF:xpsobjectmodel.IXpsOMPath.GetAccessibilityLongDescription
title: IXpsOMPath::GetAccessibilityLongDescription (xpsobjectmodel.h)
author: windows-sdk-content
description: Gets the long (detailed) textual description of the object's contents.
old-location: xps\ixpsompath_getaccessibilitylongdescription.htm
tech.root: printdocs
ms.assetid: 0ec32c0c-c6d3-4de0-a896-bf191805e799
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetAccessibilityLongDescription, GetAccessibilityLongDescription method [XPS Documents and Packaging], GetAccessibilityLongDescription method [XPS Documents and Packaging],IXpsOMPath interface, IXpsOMPath interface [XPS Documents and Packaging],GetAccessibilityLongDescription method, IXpsOMPath.GetAccessibilityLongDescription, IXpsOMPath::GetAccessibilityLongDescription, xps.ixpsompath_getaccessibilitylongdescription, xpsobjectmodel/IXpsOMPath::GetAccessibilityLongDescription
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
 - IXpsOMPath.GetAccessibilityLongDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMPath::GetAccessibilityLongDescription


## -description


Gets the long (detailed) textual description of the object's contents. This description is used by accessibility clients to describe the object.


## -parameters




### -param longDescription [out, retval]

The detailed textual description of the object's contents. If this text has not been set, a <b>NULL</b> pointer will be returned.


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
<i>longDescription</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The value returned in <i>longDescription</i> is the value of the  <b>AutomationProperties.HelpText</b> attribute of the <b>Path</b> element in the document markup.

This method allocates the memory used by the string that is returned in <i>longDescription</i>.  If <i>longDescription</i> is not <b>NULL</b>, use the <a href="https://msdn.microsoft.com/en-us/library/ms680722(v=VS.85).aspx">CoTaskMemFree</a> function  to free the memory.




## -see-also




<a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

