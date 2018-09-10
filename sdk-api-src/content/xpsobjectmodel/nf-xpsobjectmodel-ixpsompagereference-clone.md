---
UID: NF:xpsobjectmodel.IXpsOMPageReference.Clone
title: IXpsOMPageReference::Clone
author: windows-sdk-content
description: Makes a deep copy of the interface.
old-location: xps\ixpsompagereference_clone.htm
tech.root: printdocs
ms.assetid: 30511ddc-19c3-4122-864d-c368df9619a3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Clone, Clone method [XPS Documents and Packaging], Clone method [XPS Documents and Packaging],IXpsOMPageReference interface, IXpsOMPageReference interface [XPS Documents and Packaging],Clone method, IXpsOMPageReference.Clone, IXpsOMPageReference::Clone, xps.ixpsompagereference_clone, xpsobjectmodel/IXpsOMPageReference::Clone
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
 - IXpsOMPageReference.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPageReference::Clone


## -description


Makes a deep copy of the interface.


## -parameters




### -param pageReference [out, retval]

A pointer to the copy of the interface.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pageReference</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method does not update the resource pointers in the new <a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a>  interface.




## -see-also




<a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

