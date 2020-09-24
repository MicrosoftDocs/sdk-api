---
UID: NN:ocidl.IFontDisp
title: IFontDisp (ocidl.h)
description: Exposes a font object's properties through Automation. It provides a subset of the IFont methods.
helpviewer_keywords: ["IFontDisp","IFontDisp interface [COM]","IFontDisp interface [COM]","described","_ctrl_ifontdisp","com.ifontdisp","ocidl/IFontDisp"]
old-location: com\ifontdisp.htm
tech.root: com
ms.assetid: c2ee251e-2419-4436-96e4-caaf6acc2550
ms.date: 12/05/2018
ms.keywords: IFontDisp, IFontDisp interface [COM], IFontDisp interface [COM],described, _ctrl_ifontdisp, com.ifontdisp, ocidl/IFontDisp
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFontDisp
 - ocidl/IFontDisp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IFontDisp
---

# IFontDisp interface


## -description

Exposes a font object's properties through Automation. It provides a subset of the <a href="/windows/desktop/api/ocidl/nn-ocidl-ifont">IFont</a> methods.

## -remarks

The following table describes the dispIDs for the various font properties.

<table>
<tr>
<th>Constant</th>
<th>Value</th>
</tr>
<tr>
<td>DISPID_FONT_NAME

</td>
<td>0</td>
</tr>
<tr>
<td>DISPID_FONT_SIZE
</td>
<td>2</td>
</tr>
<tr>
<td>DISPID_FONT_BOLD
</td>
<td>3</td>
</tr>
<tr>
<td>DISPID_FONT_ITALIC
</td>
<td>4</td>
</tr>
<tr>
<td>DISPID_FONT_UNDER
</td>
<td>5</td>
</tr>
<tr>
<td>DISPID_FONT_STRIKE
</td>
<td>6</td>
</tr>
<tr>
<td>DISPID_FONT_WEIGHT
</td>
<td>7</td>
</tr>
<tr>
<td>DISPID_FONT_CHARSET
</td>
<td>8</td>
</tr>
</table>
 

Each property in the <b>IFontDisp</b> interface includes a <b>get_PropertyName</b> method if the property supports read access and a <b>put_PropertyName</b> method if the property supports write access. These properties support both read and write access.

<table>
<tr>
<th>Property</th>
<th>Type</th>
<th>Access</th>
<th>Description</th>
</tr>
<tr>
<td>Name</td>
<td><b>BSTR</b></td>
<td>RW</td>
<td>The facename of the font, e.g. Arial.
</td>
</tr>
<tr>
<td>Size</td>
<td><b>CY</b></td>
<td>RW</td>
<td>The point size of the font, expressed in a <b>CY</b> type to allow for fractional point sizes.
</td>
</tr>
<tr>
<td>Bold</td>
<td><b>BOOL</b></td>
<td>RW</td>
<td>Indicates whether the font is boldfaced.
</td>
</tr>
<tr>
<td>Italic</td>
<td><b>BOOL</b></td>
<td>RW</td>
<td>Indicates whether the font is italicized.
</td>
</tr>
<tr>
<td>Underline</td>
<td><b>BOOL</b></td>
<td>RW</td>
<td>Indicates whether the font is underlined.
</td>
</tr>
<tr>
<td>Strikethrough</td>
<td><b>BOOL</b></td>
<td>RW</td>
<td>Indicates whether the font is strikethrough.
</td>
</tr>
<tr>
<td>Weight</td>
<td><b>short</b></td>
<td>RW</td>
<td>The boldness of the font.
</td>
</tr>
<tr>
<td>Charset</td>
<td><b>short</b></td>
<td>RW</td>
<td>The character set used in the font, such as ANSI_CHARSET, DEFAULT_CHARSET, or SYMBOL_CHARSET.
</td>
</tr>
</table>
 

<h3><a id="OLE_Implementation"></a><a id="ole_implementation"></a><a id="OLE_IMPLEMENTATION"></a>OLE Implementation</h3>
The system provides a standard implementation of a font object with the <b>IFontDisp</b> interface on top of the underlying system font support. A font object is created through the function <a href="/windows/desktop/api/olectl/nf-olectl-olecreatefontindirect">OleCreateFontIndirect</a>. A font object supports a number of read/write properties as well as a set of methods through its interface <a href="/windows/desktop/api/ocidl/nn-ocidl-ifont">IFont</a> and supports the same set of properties (but not the methods) through a dispatch interface <b>IFontDisp</b> which is derived from <b>IDispatch</b> to provide access to the font's properties through Automation. The system implementation of the font object supplies both interfaces.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ifont">IFont</a>