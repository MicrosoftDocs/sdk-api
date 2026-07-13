---
UID: NS:objidl.tagFORMATETC
title: FORMATETC (objidl.h)
description: Represents a generalized clipboard format.
helpviewer_keywords: ["*LPFORMATETC","FORMATETC","FORMATETC structure [COM]","LPFORMATETC","LPFORMATETC structure pointer [COM]","_ole_FORMATETC","com.formatetc","objidl/FORMATETC","objidl/LPFORMATETC"]
old-location: com\formatetc.htm
tech.root: com
ms.assetid: 4478eb9a-84a1-4f3a-8290-94b8dd20c081
ms.date: 12/05/2018
ms.keywords: '*LPFORMATETC, FORMATETC, FORMATETC structure [COM], LPFORMATETC, LPFORMATETC structure pointer [COM], _ole_FORMATETC, com.formatetc, objidl/FORMATETC, objidl/LPFORMATETC'
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FORMATETC, *LPFORMATETC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagFORMATETC
 - objidl/tagFORMATETC
 - LPFORMATETC
 - objidl/LPFORMATETC
 - FORMATETC
 - objidl/FORMATETC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ObjIdl.h
api_name:
 - FORMATETC
---

# FORMATETC structure


## -description

Represents a generalized clipboard format. It is enhanced to encompass a target device, the aspect or view of the data, and a storage medium indicator. Where one might expect to find a clipboard format, OLE uses a <b>FORMATETC</b> data structure instead. This structure is used as a parameter in OLE functions and methods that require data format information.

## -struct-fields

### -field cfFormat

The clipboard format of interest. There are three types of formats recognized by OLE:


<ul>
<li>Standard interchange formats, such as CF_TEXT.
</li>
<li>Private application formats understood only by the application offering the format, or by other applications offering similar features.
</li>
<li>OLE formats, which are used to create linked or embedded objects.
</li>
</ul>

### -field ptd

A pointer to a <a href="/windows/desktop/api/objidl/ns-objidl-dvtargetdevice">DVTARGETDEVICE</a> structure containing information about the target device for which the data is being composed. A <b>NULL</b> value is used whenever the specified data format is independent of the target device or when the caller doesn't care what device is used. In the latter case, if the data requires a target device, the object should pick an appropriate default device (often the display for visual components). Data obtained from an object with a <b>NULL</b> target device, such as most metafiles, is independent of the target device. The resulting data is usually the same as it would be if the user chose the <b>Save As</b> command from the <b>File</b> menu and selected an interchange format.

### -field dwAspect

Indicates how much detail should be contained in the rendering. This parameter should be one of the <a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a> enumeration values. A single clipboard format can support multiple aspects or views of the object. Most data and presentation transfer and caching methods pass aspect information. For example, a caller might request an object's iconic picture, using the metafile clipboard format to retrieve it. Note that only one <b>DVASPECT</b> value can be used in <b>dwAspect</b>. That is, <b>dwAspect</b> cannot be the result of a Boolean OR operation on several <b>DVASPECT</b> values.

### -field lindex

Part of the aspect when the data must be split across page boundaries. The most common value is -1, which identifies all of the data. Zero-based index should be used for <a href="/windows/win32/shell/clipboard">CFSTR_FILECONTENTS</a> format. For the aspects DVASPECT_THUMBNAIL and DVASPECT_ICON, lindex is ignored.

### -field tymed

One of the <a href="/windows/desktop/api/objidl/ne-objidl-tymed">TYMED</a> enumeration constants which indicate the type of storage medium used to transfer the object's data. Data can be transferred using whatever medium makes sense for the object. For example, data can be passed using global memory, a disk file, or structured storage objects. For more information, see the <b>TYMED</b> enumeration.

## -remarks

The <b>FORMATETC</b> structure is used by methods in the data transfer and presentation interfaces as a parameter specifying the data being transferred. For example, the <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a> method uses the <b>FORMATETC</b> structure to indicate exactly what kind of data the caller is requesting.

## -see-also

<a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a>



<a href="/windows/desktop/api/objidl/nn-objidl-idataadviseholder">IDataAdviseHolder</a>



<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ienumformatetc">IEnumFORMATETC</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-iolecache">IOleCache</a>



<a href="/windows/desktop/api/ole/nf-ole-olecreate">OleCreate</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olecreatefromdata">OleCreateFromData</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olecreatelink">OleCreateLink</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olecreatelinkfromdata">OleCreateLinkFromData</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olecreatelinktofile">OleCreateLinkToFile</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olecreatestaticfromdata">OleCreateStaticFromData</a>



<a href="/windows/desktop/api/objidl/ns-objidl-statdata">STATDATA</a>



<a href="/windows/win32/api/objidl/ns-objidl-ustgmedium-r1">STGMEDIUM</a>



<a href="/windows/desktop/api/objidl/ne-objidl-tymed">TYMED</a>