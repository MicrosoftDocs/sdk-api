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
f1_keywords:
- ocidl/IPicture
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- OCIdl.h
api_name:
- IPicture
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPicture interface


## -description


Manages a picture object and its properties. Picture objects provide a language-neutral abstraction for bitmaps, icons, and metafiles. As with the standard font object, the system provides a standard implementation of the picture object. Its primary interfaces are <b>IPicture</b> and <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ipicturedisp">IPictureDisp</a>, the latter being derived from <b>IDispatch</b> to provide access to the picture's properties through Automation. A picture object is created with <a href="https://docs.microsoft.com/windows/desktop/api/olectl/nf-olectl-olecreatepictureindirect">OleCreatePictureIndirect</a>.

The picture object also supports the outgoing interface <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ipropertynotifysink">IPropertyNotifySink</a>, so a client can determine when picture properties change. Because the picture object supports at least one outgoing interface, it also implements <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a> and its associated interfaces for this purpose.

The picture object also supports <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a> so that it can save and load itself from an instance of <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>. An object that uses a picture object internally would normally save and load the picture as part of the object's own persistence handling. The function <a href="https://docs.microsoft.com/windows/desktop/api/olectl/nf-olectl-oleloadpicture">OleLoadPicture</a> simplifies the creation of a picture object based on stream contents.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPicture</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPicture</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPicture</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipicture-get_attributes">get_Attributes</a>
</td>
<td align="left" width="63%">
Retrieves the current set of the picture's bit attributes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipicture-get_curdc">get_CurDC</a>
</td>
<td align="left" width="63%">
Retrieves the current device context into which this picture is selected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipicture-get_handle">get_Handle</a>
</td>
<td align="left" width="63%">
Retrieves a handle to the picture managed within this picture object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipicture-get_height">get_Height</a>
</td>
<td align="left" width="63%">
Retrieves the current height of the picture in the picture object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipicture-get_hpal">get_hPal</a>
</td>
<td align="left" width="63%">
Retrieves the current palette of the picture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipicture-get_keeporiginalformat">get_KeepOriginalFormat</a>
</td>
<td align="left" width="63%">
Retrieves the current value of the picture object's KeepOriginalFormat property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipicture-get_type">get_Type</a>
</td>
<td align="left" width="63%">
Retrieves the current type of the picture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipicture-get_width">get_Width</a>
</td>
<td align="left" width="63%">
Retrieves the current width of the picture in the picture object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipicture-picturechanged">PictureChanged</a>
</td>
<td align="left" width="63%">
Notifies the picture object that its picture resource changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipicture-put_keeporiginalformat">put_KeepOriginalFormat</a>
</td>
<td align="left" width="63%">
Sets the picture object's KeepOriginalFormat property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipicture-render">Render</a>
</td>
<td align="left" width="63%">
Draws the specified portion of the picture onto the specified device context, positioned at the specified location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipicture-saveasfile">SaveAsFile</a>
</td>
<td align="left" width="63%">
Saves the picture's data into a stream in the same format that it would save itself into a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipicture-selectpicture">SelectPicture</a>
</td>
<td align="left" width="63%">
Selects a bitmap picture into a given device context, returning the device context in which the picture was previously selected as well as the picture's handle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipicture-set_hpal">set_hPal</a>
</td>
<td align="left" width="63%">
Sets the current palette of the picture.

</td>
</tr>
</table> 


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
<td>The type of picture (see <a href="https://docs.microsoft.com/windows/desktop/com/pictype-constants">PICTYPE</a>).
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
Picture objects provide a language-neutral abstraction for bitmaps, icons, and metafiles. As with the standard font object, the system provides a standard implementation of the picture object. Its primary interfaces are <b>IPicture</b> and <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ipicturedisp">IPictureDisp</a>. A picture object is created with <a href="https://docs.microsoft.com/windows/desktop/api/olectl/nf-olectl-olecreatepictureindirect">OleCreatePictureIndirect</a> and supports both the <b>IPicture</b> and the <b>IPictureDisp</b> interfaces.

The OLE-provided picture object implements the complete semantics of the <b>IPicture</b> and <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ipicturedisp">IPictureDisp</a> interfaces.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ipicturedisp">IPictureDisp</a>
 

 

