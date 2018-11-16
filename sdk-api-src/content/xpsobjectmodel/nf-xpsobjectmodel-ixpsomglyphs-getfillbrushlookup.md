---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.GetFillBrushLookup
title: IXpsOMGlyphs::GetFillBrushLookup
author: windows-sdk-content
description: Gets the lookup key of the IXpsOMBrush interface that is stored in a resource dictionary and will be used as the fill brush.
old-location: xps\ixpsomglyphs_getfillbrushlookup.htm
tech.root: printdocs
ms.assetid: f71b0b98-12d6-4108-8b1e-4ad254ffbdfd
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetFillBrushLookup, GetFillBrushLookup method [XPS Documents and Packaging], GetFillBrushLookup method [XPS Documents and Packaging],IXpsOMGlyphs interface, IXpsOMGlyphs interface [XPS Documents and Packaging],GetFillBrushLookup method, IXpsOMGlyphs.GetFillBrushLookup, IXpsOMGlyphs::GetFillBrushLookup, xps.ixpsomglyphs_getfillbrushlookup, xpsobjectmodel/IXpsOMGlyphs::GetFillBrushLookup
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
 - IXpsOMGlyphs.GetFillBrushLookup
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
- IXpsOMGlyphs.GetFillBrushLookup
: 
---

# IXpsOMGlyphs::GetFillBrushLookup


## -description


Gets the lookup key of the <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a> interface that is stored in a resource dictionary and will be used as the fill brush.


## -parameters




### -param key [out, retval]

The lookup key for the brush that is stored in a resource dictionary and will be used as the fill brush. If a fill brush lookup key has not been set or if a local fill brush has been set, a <b>NULL</b> pointer will be returned.

<table>
<tr>
<th>Most recent method called</th>
<th>String that is returned in <i>key</i></th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/73d1b0c2-81f9-4b1e-85fa-22e1e1c221f3">SetFillBrushLocal</a>


</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/a983583b-8698-48aa-af24-2e71d87d30c4">SetFillBrushLookup</a>


</td>
<td>
The lookup key that is set by <a href="https://msdn.microsoft.com/a983583b-8698-48aa-af24-2e71d87d30c4">SetFillBrushLookup</a>.

</td>
</tr>
<tr>
<td>
Neither <a href="https://msdn.microsoft.com/73d1b0c2-81f9-4b1e-85fa-22e1e1c221f3">SetFillBrushLocal</a> nor <a href="https://msdn.microsoft.com/a983583b-8698-48aa-af24-2e71d87d30c4">SetFillBrushLookup</a> has been called yet.

</td>
<td>
<b>NULL</b> pointer.

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
<i>key</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method allocates the memory that is used by the string returned in <i>key</i>.  If <i>key</i> is not <b>NULL</b>, use the <a href="https://msdn.microsoft.com/en-us/library/ms680722(v=VS.85).aspx">CoTaskMemFree</a> function  to free the memory.




## -see-also




<a href="https://msdn.microsoft.com/6d2cda65-c719-46f2-97c9-8aee7b5f84b9">IXpsOMGlyphs</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

