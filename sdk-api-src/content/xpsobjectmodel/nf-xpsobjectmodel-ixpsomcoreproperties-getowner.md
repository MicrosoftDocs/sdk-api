---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.GetOwner
title: IXpsOMCoreProperties::GetOwner method
author: windows-driver-content
description: Gets a pointer to the IXpsOMPackage interface that contains the core properties.
old-location: xps\ixpsomcoreproperties_getowner.htm
old-project: printdocs
ms.assetid: e3b2b9a7-7498-48a1-9d1f-eb954dc5576c
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetOwner method [XPS Documents and Packaging], GetOwner method [XPS Documents and Packaging], IXpsOMCoreProperties interface, GetOwner,IXpsOMCoreProperties.GetOwner, IXpsOMCoreProperties, IXpsOMCoreProperties interface [XPS Documents and Packaging], GetOwner method, IXpsOMCoreProperties::GetOwner, xps.ixpsomcoreproperties_getowner, xpsobjectmodel/IXpsOMCoreProperties::GetOwner
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IXpsOMCoreProperties.GetOwner
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMCoreProperties::GetOwner method


## -description


Gets a pointer to the <a href="https://msdn.microsoft.com/7b0a36d6-1af1-4c2c-af14-d6139e9115c3">IXpsOMPackage</a> interface that contains the core properties.


## -parameters




### -param package [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/7b0a36d6-1af1-4c2c-af14-d6139e9115c3">IXpsOMPackage</a> interface that contains the core properties.  If the interface does not belong to a package, a <b>NULL</b> pointer is returned.


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
<i>package</i> was <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/705ec9c7-5aa9-4fc5-ad2c-441cb545d056">IXpsOMCoreProperties</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">Standard ECMA-376, Office Open XML File Formats</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

