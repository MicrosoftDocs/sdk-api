---
UID: NN:ocidl.IPictureDisp
title: IPictureDisp (ocidl.h)
description: Exposes the picture object's properties through Automation. It provides a subset of the functionality available through IPicture methods.
helpviewer_keywords: ["IPictureDisp","IPictureDisp interface [COM]","IPictureDisp interface [COM]","described","_ctrl_ipicturedisp","com.ipicturedisp","ocidl/IPictureDisp"]
old-location: com\ipicturedisp.htm
tech.root: com
ms.assetid: 42efa5a3-66af-4432-a2fd-616261b1f407
ms.date: 12/05/2018
ms.keywords: IPictureDisp, IPictureDisp interface [COM], IPictureDisp interface [COM],described, _ctrl_ipicturedisp, com.ipicturedisp, ocidl/IPictureDisp
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
 - IPictureDisp
 - ocidl/IPictureDisp
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
 - IPictureDisp
---

# IPictureDisp interface


## -description

Exposes the picture object's properties through Automation. It provides a subset of the functionality available through <a href="/windows/desktop/api/ocidl/nn-ocidl-ipicture">IPicture</a> methods.

## -remarks

The following table describes the dispIDs for the various picture properties.

<table>
<tr>
<th>Constant</th>
<th>Value</th>
</tr>
<tr>
<td>DISPID_PICT_HANDLE
</td>
<td>0</td>
</tr>
<tr>
<td>DISPID_PICT_HPAL
</td>
<td>2</td>
</tr>
<tr>
<td>DISPID_PICT_TYPE
</td>
<td>3</td>
</tr>
<tr>
<td>DISPID_PICT_WIDTH
</td>
<td>4</td>
</tr>
<tr>
<td>DISPID_PICT_HEIGHT
</td>
<td>5</td>
</tr>
<tr>
<td>DISPID_PICT_RENDER
</td>
<td>6</td>
</tr>
</table>
 

Each property in the <b>IPictureDisp</b> interface includes a <b>get_PropertyName</b> method if the property supports read access and a <b>put_PropertyName</b> method if the property supports write access. Most of the properties support read access only with the exception of the hPal property.

<table>
<tr>
<th>Property</th>
<th>Type</th>
<th>Access</th>
<th>Description</th>
</tr>
<tr>
<td>Handle</td>
<td><b>OLE_HANDLE</b> (<b>int</b>)
</td>
<td>R</td>
<td>The Windows GDI handle of the picture
</td>
</tr>
<tr>
<td>hPal</td>
<td><b>OLE_HANDLE</b> (<b>int</b>)
</td>
<td>RW</td>
<td>The Windows handle of the palette used by the picture.
</td>
</tr>
<tr>
<td>Type</td>
<td><b>short</b></td>
<td>R</td>
<td>The type of picture (see <a href="/windows/desktop/com/pictype-constants">PICTYPE</a>).
</td>
</tr>
<tr>
<td>Width</td>
<td><b>OLE_XSIZE_HIMETRIC</b> (<b>long</b>)
</td>
<td>R</td>
<td>The width of the picture.
</td>
</tr>
<tr>
<td>Height</td>
<td><b>OLE_YSIZE_HIMETRIC</b> (<b>long</b>)
</td>
<td>R</td>
<td>The height of the picture.
</td>
</tr>
</table>
 

<h3><a id="OLE_Implementation"></a><a id="ole_implementation"></a><a id="OLE_IMPLEMENTATION"></a>OLE Implementation</h3>
Picture objects provide a language-neutral abstraction for bitmaps, icons, and metafiles. As with the standard font object, the system provides a standard implementation of the picture object. Its primary interfaces are <a href="/windows/desktop/api/ocidl/nn-ocidl-ipicture">IPicture</a> and <b>IPictureDisp</b>. A picture object is created with <a href="/windows/desktop/api/olectl/nf-olectl-olecreatepictureindirect">OleCreatePictureIndirect</a> and supports both the <b>IPicture</b> and the <b>IPictureDisp</b> interfaces.

The OLE-provided picture object implements the complete semantics of the <a href="/windows/desktop/api/ocidl/nn-ocidl-ipicture">IPicture</a> and <b>IPictureDisp</b> interfaces.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipicture">IPicture</a>