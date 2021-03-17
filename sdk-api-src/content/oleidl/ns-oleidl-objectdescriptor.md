---
UID: NS:oleidl.tagOBJECTDESCRIPTOR
title: OBJECTDESCRIPTOR (oleidl.h)
description: Represents the data structure used for the CF_OBJECTDESRIPTOR and CF_LINKSRCDESCRIPTOR file formats.
helpviewer_keywords: ["*LPLINKSRCDESCRIPTOR","*LPOBJECTDESCRIPTOR","*PLINKSRCDESCRIPTOR","*POBJECTDESCRIPTOR","LINKSRCDESCRIPTOR","LPOBJECTDESCRIPTOR","LPOBJECTDESCRIPTOR structure pointer [COM]","OBJECTDESCRIPTOR","OBJECTDESCRIPTOR structure [COM]","POBJECTDESCRIPTOR","POBJECTDESCRIPTOR structure pointer [COM]","_ole_OBJECTDESCRIPTOR","com.objectdescriptor","oleidl/LPOBJECTDESCRIPTOR","oleidl/OBJECTDESCRIPTOR","oleidl/POBJECTDESCRIPTOR"]
old-location: com\objectdescriptor.htm
tech.root: com
ms.assetid: 5865e16b-c1a5-4bfd-8d94-c2f8f73b1205
ms.date: 12/05/2018
ms.keywords: '*LPLINKSRCDESCRIPTOR, *LPOBJECTDESCRIPTOR, *PLINKSRCDESCRIPTOR, *POBJECTDESCRIPTOR, LINKSRCDESCRIPTOR, LPOBJECTDESCRIPTOR, LPOBJECTDESCRIPTOR structure pointer [COM], OBJECTDESCRIPTOR, OBJECTDESCRIPTOR structure [COM], POBJECTDESCRIPTOR, POBJECTDESCRIPTOR structure pointer [COM], _ole_OBJECTDESCRIPTOR, com.objectdescriptor, oleidl/LPOBJECTDESCRIPTOR, oleidl/OBJECTDESCRIPTOR, oleidl/POBJECTDESCRIPTOR'
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: OBJECTDESCRIPTOR, *POBJECTDESCRIPTOR, *LPOBJECTDESCRIPTOR, LINKSRCDESCRIPTOR, *PLINKSRCDESCRIPTOR, *LPLINKSRCDESCRIPTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOBJECTDESCRIPTOR
 - oleidl/tagOBJECTDESCRIPTOR
 - POBJECTDESCRIPTOR
 - oleidl/POBJECTDESCRIPTOR
 - OBJECTDESCRIPTOR
 - oleidl/OBJECTDESCRIPTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OleIdl.h
api_name:
 - OBJECTDESCRIPTOR
---

# OBJECTDESCRIPTOR structure


## -description

Represents the data structure used for the CF_OBJECTDESRIPTOR and CF_LINKSRCDESCRIPTOR file formats. These formats provide user interface information during data transfer operations, for example, the <b>Paste Special</b> dialog box or target feedback information during drag-and-drop operations.

## -struct-fields

### -field cbSize

The size of structure, in bytes.

### -field clsid

The CLSID of the object being transferred. The clsid is used to obtain the icon for the <b>Display As Icon</b> option in the <b>Paste Special</b> dialog box and is applicable only if the Embed Source or Embedded Object formats are offered. If neither is offered, the value of clsid should be CLSID_NULL. The clsid can be retrieved by the source by loading the object and calling the <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getuserclassid">IOleObject::GetUserClassID</a> method. Note that for link objects, this value is not the same as the value returned by the <a href="/windows/desktop/api/objidl/nf-objidl-ipersist-getclassid">IPersist::GetClassID</a> method.

### -field dwDrawAspect

The display aspect of the object. Typically, this value is DVASPECT_CONTENT or DVASPECT_ICON. If the source application did not draw the object originally, the <b>dwDrawAspect</b> field contains a zero value (which is not the same as DVASPECT_CONTENT). For more information, see <a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a>.

### -field sizel

The true extent of the object (without cropping or scaling) in <b>HIMETRIC</b> units. Setting this field is optional. The value can be (0,0) for applications that do not draw the object being transferred. This field is used primarily by targets of drag-and-drop operations, so they can give appropriate feedback to the user.

### -field pointl

The offset in <b>HIMETRIC</b> units from the upper-left corner of the object where a drag-and-drop operation was initiated. This field is only meaningful for a drag-and-drop transfer operation since it corresponds to the point where the mouse was clicked to initiate the drag-and-drop operation. The value is (0,0) for other transfer situations, such as a clipboard copy and paste.

### -field dwStatus

The copy of the status flags for the object. These flags are defined by the <a href="/windows/desktop/api/oleidl/ne-oleidl-olemisc">OLEMISC</a> enumeration. If an embedded object is being transferred, they are returned by calling the <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getmiscstatus">IOleObject::GetMiscStatus</a> method.

### -field dwFullUserTypeName

The offset for finding the full user type name of the object being transferred. It specifies the offset, in bytes, from the beginning of the <b>OBJECTDESCRIPTOR</b> data structure to the null-terminated string that specifies the full user type name of the object being transferred. The value is zero if the string is not present. This string is used by the destination of a data transfer to create labels in the <b>Paste Special</b> dialog box. The destination application must be able to handle the cases when this string is omitted.

### -field dwSrcOfCopy

The offset, in bytes, from the beginning of the data structure to the null-terminated string that specifies the source of the transfer. The <b>dwSrcOfCopy</b> member is typically implemented as the display name of the temporary moniker that identifies the data source. The value for <b>dwSrcOfCopy</b> is displayed in the Source line of the <b>Paste Special</b> dialog box. A zero value indicates that the string is not present. If <b>dwSrcOfCopy</b> is zero, the string "Unknown Source" is displayed in the <b>Paste Special</b> dialog box.

## -see-also

<a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a>



<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>