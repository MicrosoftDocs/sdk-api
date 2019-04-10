---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.GetUnicodeString
title: IXpsOMGlyphs::GetUnicodeString (xpsobjectmodel.h)
author: windows-sdk-content
description: Gets the text in unescaped UTF-16 scalar values.
old-location: xps\ixpsomglyphs_getunicodestring.htm
tech.root: printdocs
ms.assetid: 0b1573b5-c9c7-4c7b-8511-c5c2fc42ed3e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetUnicodeString, GetUnicodeString method [XPS Documents and Packaging], GetUnicodeString method [XPS Documents and Packaging],IXpsOMGlyphs interface, IXpsOMGlyphs interface [XPS Documents and Packaging],GetUnicodeString method, IXpsOMGlyphs.GetUnicodeString, IXpsOMGlyphs::GetUnicodeString, xps.ixpsomglyphs_getunicodestring, xpsobjectmodel/IXpsOMGlyphs::GetUnicodeString
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
 - IXpsOMGlyphs.GetUnicodeString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMGlyphs::GetUnicodeString


## -description


Gets the text in unescaped UTF-16 scalar values.


## -parameters




### -param unicodeString [out, retval]

The UTF-16 Unicode string of the text to be displayed. If the string is empty, a <b>NULL</b> pointer is returned.


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



This method allocates the memory that is used by the string returned in <i>unicodeString</i>.  If <i>unicodeString</i> is not <b>NULL</b>, use the <a href="https://msdn.microsoft.com/en-us/library/ms680722(v=VS.85).aspx">CoTaskMemFree</a> function  to free the memory.




## -see-also




<a href="https://msdn.microsoft.com/6d2cda65-c719-46f2-97c9-8aee7b5f84b9">IXpsOMGlyphs</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

