---
UID: NF:xpsobjectmodel.IXpsOMVisual.GetIsHyperlinkTarget
title: IXpsOMVisual::GetIsHyperlinkTarget
author: windows-sdk-content
description: Gets a value that indicates whether the visual is the target of a hyperlink.
old-location: xps\ixpsomvisual_getishyperlinktarget.htm
old-project: printdocs
ms.assetid: bd6047a6-d6ba-4c62-8f4c-0348e3281d75
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: FALSE, GetIsHyperlinkTarget, GetIsHyperlinkTarget method [XPS Documents and Packaging], GetIsHyperlinkTarget method [XPS Documents and Packaging],IXpsOMVisual interface, IXpsOMVisual interface [XPS Documents and Packaging],GetIsHyperlinkTarget method, IXpsOMVisual.GetIsHyperlinkTarget, IXpsOMVisual::GetIsHyperlinkTarget, TRUE, xps.ixpsomvisual_getishyperlinktarget, xpsobjectmodel/IXpsOMVisual::GetIsHyperlinkTarget
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
 - IXpsOMVisual.GetIsHyperlinkTarget
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMVisual::GetIsHyperlinkTarget


## -description


Gets a value that indicates whether the visual is the target of a hyperlink.


## -parameters




### -param isHyperlink [out, retval]

The Boolean value that indicates whether the visual is the target of a hyperlink.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
The visual is the target of a hyperlink.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
The visual is not the target of a hyperlink.

</td>
</tr>
</table>
 


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
<i>isHyperlink</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

