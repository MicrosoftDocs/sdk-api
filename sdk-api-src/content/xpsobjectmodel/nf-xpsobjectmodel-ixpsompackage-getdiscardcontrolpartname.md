---
UID: NF:xpsobjectmodel.IXpsOMPackage.GetDiscardControlPartName
title: IXpsOMPackage::GetDiscardControlPartName
author: windows-sdk-content
description: Gets the name of the discard control part in the XPS package.
old-location: xps\ixpsompackage_getdiscardcontrolpartname.htm
tech.root: printdocs
ms.assetid: e1c60001-0a0c-4ff9-bb17-fef3e47b16a6
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetDiscardControlPartName, GetDiscardControlPartName method [XPS Documents and Packaging], GetDiscardControlPartName method [XPS Documents and Packaging],IXpsOMPackage interface, IXpsOMPackage interface [XPS Documents and Packaging],GetDiscardControlPartName method, IXpsOMPackage.GetDiscardControlPartName, IXpsOMPackage::GetDiscardControlPartName, xps.ixpsompackage_getdiscardcontrolpartname, xpsobjectmodel/IXpsOMPackage::GetDiscardControlPartName
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
 - IXpsOMPackage.GetDiscardControlPartName
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
- IXpsOMPackage.GetDiscardControlPartName
: 
---

# IXpsOMPackage::GetDiscardControlPartName


## -description


Gets the name of the discard control part in the XPS package.


## -parameters




### -param discardControlPartUri [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface that contains the name of the discard control part in the XPS package. If a discard control part has not been set, a <b>NULL</b> pointer is returned.


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
<i>discardControlPartUri</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/7b0a36d6-1af1-4c2c-af14-d6139e9115c3">IXpsOMPackage</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

