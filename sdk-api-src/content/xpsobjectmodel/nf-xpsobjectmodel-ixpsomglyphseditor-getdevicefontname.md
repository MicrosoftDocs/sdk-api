---
UID: NF:xpsobjectmodel.IXpsOMGlyphsEditor.GetDeviceFontName
title: IXpsOMGlyphsEditor::GetDeviceFontName
author: windows-sdk-content
description: Gets the name of the device font.
old-location: xps\ixpsomglyphseditor_getdevicefontname.htm
old-project: printdocs
ms.assetid: 79d1c913-0ed9-47bc-a06c-566a0ec19760
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: GetDeviceFontName, GetDeviceFontName method [XPS Documents and Packaging], GetDeviceFontName method [XPS Documents and Packaging],IXpsOMGlyphsEditor interface, IXpsOMGlyphsEditor interface [XPS Documents and Packaging],GetDeviceFontName method, IXpsOMGlyphsEditor.GetDeviceFontName, IXpsOMGlyphsEditor::GetDeviceFontName, xps.ixpsomglyphseditor_getdevicefontname, xpsobjectmodel/IXpsOMGlyphsEditor::GetDeviceFontName
ms.prod: windows
ms.technology: windows-sdk
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
 - IXpsOMGlyphsEditor.GetDeviceFontName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGlyphsEditor::GetDeviceFontName


## -description


Gets the name of the  device font.


## -parameters




### -param deviceFontName [out, retval]

The name of the device font; if not specified, a <b>NULL</b> pointer will be returned.


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
<i>deviceFontName</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The  device font name is created as an escaped  name when the object is serialized.

The device font name uniquely identifies a specific device font and is typically defined by a hardware or font vendor.

This method allocates the memory used by the string that is returned in <i>deviceFontName</i>.  If <i>deviceFontName</i> is not <b>NULL</b>, use the <a href="_com_CoTaskMemFree">CoTaskMemFree</a> function  to free the memory.




## -see-also




<a href="https://msdn.microsoft.com/5bdf2892-ce6f-4560-b638-e441166fc309">IXpsOMGlyphsEditor</a>
 

 

