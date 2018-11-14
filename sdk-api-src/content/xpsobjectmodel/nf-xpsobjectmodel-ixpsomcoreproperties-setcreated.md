---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.SetCreated
title: IXpsOMCoreProperties::SetCreated
author: windows-sdk-content
description: Sets the created property.
old-location: xps\ixpsomcoreproperties_setcreated.htm
tech.root: printdocs
ms.assetid: 1a71d338-a34e-40df-ade0-130cd8e0a176
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IXpsOMCoreProperties interface [XPS Documents and Packaging],SetCreated method, IXpsOMCoreProperties.SetCreated, IXpsOMCoreProperties::SetCreated, SetCreated, SetCreated method [XPS Documents and Packaging], SetCreated method [XPS Documents and Packaging],IXpsOMCoreProperties interface, xps.ixpsomcoreproperties_setcreated, xpsobjectmodel/IXpsOMCoreProperties::SetCreated
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
 - IXpsOMCoreProperties.SetCreated
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
- IXpsOMCoreProperties.SetCreated
: 
---

# IXpsOMCoreProperties::SetCreated


## -description


Sets the <b>created</b> property.


## -parameters




### -param created [in]

The date and time the package was created. A <b>NULL</b> pointer clears the <b>created</b> property


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
<i>created</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The <b>created</b> property contains the date and time the package was created.




## -see-also




<a href="https://msdn.microsoft.com/705ec9c7-5aa9-4fc5-ad2c-441cb545d056">IXpsOMCoreProperties</a>



<a href="https://msdn.microsoft.com/en-us/library/ms724950(v=VS.85).aspx">SYSTEMTIME</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">Standard ECMA-376, Office Open XML File Formats</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

