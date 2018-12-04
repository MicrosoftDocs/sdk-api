---
UID: NF:xpsobjectmodel.IXpsOMPart.GetPartName
title: IXpsOMPart::GetPartName
author: windows-sdk-content
description: Gets the name that will be used when the part is serialized.
old-location: xps\ixpsompart_getpartname.htm
tech.root: printdocs
ms.assetid: 43793c60-5fa3-4895-8a6a-7e010e65ac3e
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetPartName, GetPartName method [XPS Documents and Packaging], GetPartName method [XPS Documents and Packaging],IXpsOMPart interface, IXpsOMPart interface [XPS Documents and Packaging],GetPartName method, IXpsOMPart.GetPartName, IXpsOMPart::GetPartName, xps.ixpsompart_getpartname, xpsobjectmodel/IXpsOMPart::GetPartName
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
 - IXpsOMPart.GetPartName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPart::GetPartName


## -description


Gets the name that will be used when the part is serialized.


## -parameters




### -param partUri [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface that contains the part name. If the part name has not been set (by the <a href="https://msdn.microsoft.com/d17083f3-38b2-43bd-8e87-1092cf397f29">SetPartName</a> method), a <b>NULL</b> pointer is returned.


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
<i>partUri</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/71cd0155-6c95-42ca-bfc3-dffd43d95dc9">IXpsOMPart</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

