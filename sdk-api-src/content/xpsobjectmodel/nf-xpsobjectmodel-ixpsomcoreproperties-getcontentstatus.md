---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.GetContentStatus
title: IXpsOMCoreProperties::GetContentStatus
author: windows-sdk-content
description: Gets the contentStatus property.
old-location: xps\ixpsomcoreproperties_getcontentstatus.htm
old-project: printdocs
ms.assetid: 9e058e8d-ace6-4892-87c1-07e28ff24462
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetContentStatus, GetContentStatus method [XPS Documents and Packaging], GetContentStatus method [XPS Documents and Packaging],IXpsOMCoreProperties interface, IXpsOMCoreProperties interface [XPS Documents and Packaging],GetContentStatus method, IXpsOMCoreProperties.GetContentStatus, IXpsOMCoreProperties::GetContentStatus, xps.ixpsomcoreproperties_getcontentstatus, xpsobjectmodel/IXpsOMCoreProperties::GetContentStatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.redist: 
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
 - IXpsOMCoreProperties.GetContentStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMCoreProperties::GetContentStatus


## -description


Gets the <b>contentStatus</b> property.


## -parameters




### -param contentStatus [out, retval]

The string that is read from the <b>contentStatus</b> property.


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
<i>contentStatus</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The <b>contentStatus</b> property stores the content's status. Examples of <b>contentStatus</b> values include <b>Draft</b>, <b>Reviewed</b>, and <b>Final</b>.

This method allocates the memory used by the string that is returned in <i>contentStatus</i>.  If <i>contentStatus</i> is not <b>NULL</b>, use the <a href="_com_CoTaskMemFree">CoTaskMemFree</a> function  to free the memory.




## -see-also




<a href="https://msdn.microsoft.com/705ec9c7-5aa9-4fc5-ad2c-441cb545d056">IXpsOMCoreProperties</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">Standard ECMA-376, Office Open XML File Formats</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

