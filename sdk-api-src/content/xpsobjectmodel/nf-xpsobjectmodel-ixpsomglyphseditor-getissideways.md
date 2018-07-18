---
UID: NF:xpsobjectmodel.IXpsOMGlyphsEditor.GetIsSideways
title: IXpsOMGlyphsEditor::GetIsSideways
author: windows-sdk-content
description: Gets a Boolean value that indicates whether the text is to be rendered with the glyphs rotated sideways.
old-location: xps\ixpsomglyphseditor_getissideways.htm
old-project: printdocs
ms.assetid: d115dbce-a81c-458f-8929-9e49e84a575d
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: FALSE, GetIsSideways, GetIsSideways method [XPS Documents and Packaging], GetIsSideways method [XPS Documents and Packaging],IXpsOMGlyphsEditor interface, IXpsOMGlyphsEditor interface [XPS Documents and Packaging],GetIsSideways method, IXpsOMGlyphsEditor.GetIsSideways, IXpsOMGlyphsEditor::GetIsSideways, TRUE, xps.ixpsomglyphseditor_getissideways, xpsobjectmodel/IXpsOMGlyphsEditor::GetIsSideways
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
 - IXpsOMGlyphsEditor.GetIsSideways
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGlyphsEditor::GetIsSideways


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
Rotate the glyphs sideways. Produces sideways text.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
Do not rotate the glyphs sideways. Produces normal text.

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



The default value for this property is <b>false</b>.




## -see-also




<a href="https://msdn.microsoft.com/5bdf2892-ce6f-4560-b638-e441166fc309">IXpsOMGlyphsEditor</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

