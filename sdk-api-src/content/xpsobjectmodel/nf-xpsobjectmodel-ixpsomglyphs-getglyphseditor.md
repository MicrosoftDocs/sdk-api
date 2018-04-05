---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.GetGlyphsEditor
title: IXpsOMGlyphs::GetGlyphsEditor method
author: windows-driver-content
description: Gets a pointer to the IXpsOMGlyphsEditor interface that will be used to edit the glyphs in the object.
old-location: xps\ixpsomglyphs_getglyphseditor.htm
old-project: printdocs
ms.assetid: 1c641d99-9303-484d-82e0-2d71e2c43561
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetGlyphsEditor method [XPS Documents and Packaging], GetGlyphsEditor method [XPS Documents and Packaging], IXpsOMGlyphs interface, GetGlyphsEditor,IXpsOMGlyphs.GetGlyphsEditor, IXpsOMGlyphs, IXpsOMGlyphs interface [XPS Documents and Packaging], GetGlyphsEditor method, IXpsOMGlyphs::GetGlyphsEditor, xps.ixpsomglyphs_getglyphseditor, xpsobjectmodel/IXpsOMGlyphs::GetGlyphsEditor
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
-	IXpsOMGlyphs.GetGlyphsEditor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGlyphs::GetGlyphsEditor method


## -description


Gets a pointer to the <a href="https://msdn.microsoft.com/5bdf2892-ce6f-4560-b638-e441166fc309">IXpsOMGlyphsEditor</a> interface that will be used to edit the glyphs in the object.


## -parameters




### -param editor [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/5bdf2892-ce6f-4560-b638-e441166fc309">IXpsOMGlyphsEditor</a> interface.


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
<i>editor</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



An <a href="https://msdn.microsoft.com/5bdf2892-ce6f-4560-b638-e441166fc309">IXpsOMGlyphsEditor</a>  interface is required to edit the read-only properties of the <a href="https://msdn.microsoft.com/6d2cda65-c719-46f2-97c9-8aee7b5f84b9">IXpsOMGlyphs</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/6d2cda65-c719-46f2-97c9-8aee7b5f84b9">IXpsOMGlyphs</a>



<a href="https://msdn.microsoft.com/5bdf2892-ce6f-4560-b638-e441166fc309">IXpsOMGlyphsEditor</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

