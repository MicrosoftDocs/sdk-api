---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.GetTitle
title: IXpsOMCoreProperties::GetTitle
author: windows-sdk-content
description: Gets the title property.
old-location: xps\ixpsomcoreproperties_gettitle.htm
tech.root: printdocs
ms.assetid: 32551dd2-2d6e-4aaa-864b-4c922a90fc27
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetTitle, GetTitle method [XPS Documents and Packaging], GetTitle method [XPS Documents and Packaging],IXpsOMCoreProperties interface, IXpsOMCoreProperties interface [XPS Documents and Packaging],GetTitle method, IXpsOMCoreProperties.GetTitle, IXpsOMCoreProperties::GetTitle, xps.ixpsomcoreproperties_gettitle, xpsobjectmodel/IXpsOMCoreProperties::GetTitle
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
 - IXpsOMCoreProperties.GetTitle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMCoreProperties::GetTitle


## -description


Gets the <b>title</b> property.


## -parameters




### -param title [out, retval]

The string that is read from the <b>title</b> property.


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
<i>title</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The <b>title</b> property contains the resource's name.

This method allocates the memory used by the string that is returned in <i>title</i>.  If <i>title</i> is not <b>NULL</b>, use the <a href="https://msdn.microsoft.com/en-us/library/ms680722(v=VS.85).aspx">CoTaskMemFree</a> function  to free the memory.




## -see-also




<a href="https://msdn.microsoft.com/705ec9c7-5aa9-4fc5-ad2c-441cb545d056">IXpsOMCoreProperties</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">Standard ECMA-376, Office Open XML File Formats</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

