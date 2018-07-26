---
UID: NF:xpsobjectmodel.IXpsOMGlyphsEditor.GetUnicodeString
title: IXpsOMGlyphsEditor::GetUnicodeString
author: windows-sdk-content
description: Gets the text in unescaped UTF-16 scalar values.
old-location: xps\ixpsomglyphseditor_getunicodestring.htm
old-project: printdocs
ms.assetid: 48190202-2ab4-44ad-98e0-a69e9b48576f
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: GetUnicodeString, GetUnicodeString method [XPS Documents and Packaging], GetUnicodeString method [XPS Documents and Packaging],IXpsOMGlyphsEditor interface, IXpsOMGlyphsEditor interface [XPS Documents and Packaging],GetUnicodeString method, IXpsOMGlyphsEditor.GetUnicodeString, IXpsOMGlyphsEditor::GetUnicodeString, xps.ixpsomglyphseditor_getunicodestring, xpsobjectmodel/IXpsOMGlyphsEditor::GetUnicodeString
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
 - IXpsOMGlyphsEditor.GetUnicodeString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGlyphsEditor::GetUnicodeString


## -description


Gets the text in unescaped UTF-16 scalar values.


## -parameters




### -param unicodeString [out, retval]

The UTF-16 Unicode string. If the string is empty, a <b>NULL</b> pointer is returned.


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
<i>unicodeString</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method allocates the memory used by the string that is returned in <i>unicodeString</i>.  If <i>unicodeString</i> is not <b>NULL</b>, use the <a href="https://msdn.microsoft.com/library/ms680722(v=VS.85).aspx">CoTaskMemFree</a> function  to free the memory.




## -see-also




<a href="https://msdn.microsoft.com/5bdf2892-ce6f-4560-b638-e441166fc309">IXpsOMGlyphsEditor</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

