---
UID: NN:ocidl.IPicture
title: IPicture (ocidl.h)
description: Manages a picture object and its properties. Picture objects provide a language-neutral abstraction for bitmaps, icons, and metafiles.
helpviewer_keywords: ["IPicture","IPicture interface [COM]","IPicture interface [COM]","described","_ctrl_ipicture","com.ipicture","ocidl/IPicture"]
old-location: com\ipicture.htm
tech.root: com
ms.assetid: 42e3cd0e-2413-494a-8be8-2952089e02d2
ms.date: 12/05/2018
ms.keywords: IPicture, IPicture interface [COM], IPicture interface [COM],described, _ctrl_ipicture, com.ipicture, ocidl/IPicture
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
 - IPicture
 - ocidl/IPicture
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
 - IPicture
---

# IPicture interface


## -description

Manages a picture object and its properties. Picture objects provide a language-neutral abstraction for bitmaps, icons, and metafiles. As with the standard font object, the system provides a standard implementation of the picture object. Its primary interfaces are <b>IPicture</b> and <a href="/windows/desktop/api/ocidl/nn-ocidl-ipicturedisp">IPictureDisp</a>, the latter being derived from <b>IDispatch</b> to provide access to the picture's properties through Automation. A picture object is created with <a href="/windows/desktop/api/olectl/nf-olectl-olecreatepictureindirect">OleCreatePictureIndirect</a>.

The picture object also supports the outgoing interface <a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertynotifysink">IPropertyNotifySink</a>, so a client can determine when picture properties change. Because the picture object supports at least one outgoing interface, it also implements <a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a> and its associated interfaces for this purpose.

The picture object also supports <a href="/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a> so that it can save and load itself from an instance of <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>. An object that uses a picture object internally would normally save and load the picture as part of the object's own persistence handling. The function <a href="/windows/desktop/api/olectl/nf-olectl-oleloadpicture">OleLoadPicture</a> simplifies the creation of a picture object based on stream contents.

## -inheritance

The <b>IPicture</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPicture</b> also has these types of members:

## -remarks

Each property in the <b>IPicture</b> interface includes a <b>get_PropertyName</b> method if the property supports read access and a <b>put_PropertyName</b> method if the property supports write access.

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
<tr>
<td>CurDC</td>
<td><b>HDC</b></td>
<td>R</td>
<td>The current device context.</td>
</tr>
<tr>
<td>KeepOriginalFormat</td>
<td><b>BOOL</b></td>
<td>RW</td>
<td>If <b>TRUE</b>, the picture object maintains the entire original state of the picture in memory. If <b>FALSE</b>, any state not applicable to the user's computer is discarded.</td>
</tr>
<tr>
<td>Attributes</td>
<td><b>DWORD</b></td>
<td>R</td>
<td>Miscellaneous bit attributes of the picture.</td>
</tr>
</table>
 

<h3><a id="OLE_Implementation"></a><a id="ole_implementation"></a><a id="OLE_IMPLEMENTATION"></a>OLE Implementation</h3>
Picture objects provide a language-neutral abstraction for bitmaps, icons, and metafiles. As with the standard font object, the system provides a standard implementation of the picture object. Its primary interfaces are <b>IPicture</b> and <a href="/windows/desktop/api/ocidl/nn-ocidl-ipicturedisp">IPictureDisp</a>. A picture object is created with <a href="/windows/desktop/api/olectl/nf-olectl-olecreatepictureindirect">OleCreatePictureIndirect</a> and supports both the <b>IPicture</b> and the <b>IPictureDisp</b> interfaces.

The OLE-provided picture object implements the complete semantics of the <b>IPicture</b> and <a href="/windows/desktop/api/ocidl/nn-ocidl-ipicturedisp">IPictureDisp</a> interfaces.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipicturedisp">IPictureDisp</a>
