---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.GetIsSideways
title: IXpsOMGlyphs::GetIsSideways
author: windows-driver-content
description: Gets a Boolean value that indicates whether the text is to be rendered with the glyphs rotated sideways.
old-location: xps\ixpsomglyphs_getissideways.htm
old-project: printdocs
ms.assetid: 51a0c84b-6f66-4bd5-b64c-b43ef4af8462
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: FALSE, GetIsSideways, GetIsSideways method [XPS Documents and Packaging], GetIsSideways method [XPS Documents and Packaging],IXpsOMGlyphs interface, IXpsOMGlyphs interface [XPS Documents and Packaging],GetIsSideways method, IXpsOMGlyphs.GetIsSideways, IXpsOMGlyphs::GetIsSideways, TRUE, xps.ixpsomglyphs_getissideways, xpsobjectmodel/IXpsOMGlyphs::GetIsSideways
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
-	IXpsOMGlyphs.GetIsSideways
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGlyphs::GetIsSideways


## -description


Gets a Boolean value that indicates whether the text is to be rendered with the glyphs rotated sideways.


## -parameters




### -param isSideways [out, retval]

The Boolean value that indicates whether the text is to be rendered with the glyphs rotated sideways. 

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
Render the glyphs sideways to produce sideways text.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
Do not render the glyphs sideways to produce normal text.

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
<i>isSideways</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The default value for this property is <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/6d2cda65-c719-46f2-97c9-8aee7b5f84b9">IXpsOMGlyphs</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

