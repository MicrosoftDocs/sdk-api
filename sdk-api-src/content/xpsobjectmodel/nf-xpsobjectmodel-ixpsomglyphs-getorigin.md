---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.GetOrigin
title: IXpsOMGlyphs::GetOrigin
author: windows-sdk-content
description: Gets the starting position of the text.
old-location: xps\ixpsomglyphs_getorigin.htm
old-project: printdocs
ms.assetid: ec661cff-4671-401b-9c77-5036549762af
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: GetOrigin, GetOrigin method [XPS Documents and Packaging], GetOrigin method [XPS Documents and Packaging],IXpsOMGlyphs interface, IXpsOMGlyphs interface [XPS Documents and Packaging],GetOrigin method, IXpsOMGlyphs.GetOrigin, IXpsOMGlyphs::GetOrigin, xps.ixpsomglyphs_getorigin, xpsobjectmodel/IXpsOMGlyphs::GetOrigin
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
 - IXpsOMGlyphs.GetOrigin
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGlyphs::GetOrigin


## -description


Gets the starting position of the text.


## -parameters




### -param origin [out, retval]

The <a href="https://msdn.microsoft.com/3e5f693a-a0e4-41cf-a2a6-1f61c8e189e3">XPS_POINT</a> structure that receives the starting position of the text.


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
<i>origin</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



In the units of the effective coordinate space, the origin specifies the x and y coordinates of the first glyph in the run. The glyph is placed such that its baseline and the leading edge of its advance vector intersect with the point defined by <i>origin.x</i> and <i>origin.y</i>.




## -see-also




<a href="https://msdn.microsoft.com/6d2cda65-c719-46f2-97c9-8aee7b5f84b9">IXpsOMGlyphs</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/3e5f693a-a0e4-41cf-a2a6-1f61c8e189e3">XPS_POINT</a>
 

 

