---
UID: NS:mapi.MapiFileTagExt
title: MapiFileTagExt (mapi.h)
description: A MapiFileTagExt structure specifies a message attachment's type at its creation and its current form of encoding so that it can be restored to its original type at its destination.
helpviewer_keywords: ["*lpMapiFileTagExt","MapiFileTagExt","MapiFileTagExt structure","lpMapiFileTagExt","lpMapiFileTagExt structure pointer","mapi.mapifiletagext","mapi/MapiFileTagExt","mapi/lpMapiFileTagExt"]
old-location: mapi\mapifiletagext.htm
tech.root: mapi
ms.assetid: 5f6de637-14a8-46bb-a53e-f355d7592222
ms.date: 12/05/2018
ms.keywords: '*lpMapiFileTagExt, MapiFileTagExt, MapiFileTagExt structure, lpMapiFileTagExt, lpMapiFileTagExt structure pointer, mapi.mapifiletagext, mapi/MapiFileTagExt, mapi/lpMapiFileTagExt'
req.header: mapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: MapiFileTagExt, *lpMapiFileTagExt
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lpMapiFileTagExt
 - mapi/lpMapiFileTagExt
 - MapiFileTagExt
 - mapi/MapiFileTagExt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mapi.h
api_name:
 - MapiFileTagExt
---

# MapiFileTagExt structure


## -description

A <b>MapiFileTagExt</b> structure specifies a message attachment's type at its creation and its current form of encoding so that it can be restored to its original type at its destination.

## -struct-fields

### -field ulReserved

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">ULONG</a></b>

Reserved; must be zero.

### -field cbTag

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">ULONG</a></b>

The size, in bytes, of the value defined by the <b>lpTag</b> member.

### -field lpTag

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPBYTE</a></b>

Pointer to an X.400 object identifier indicating the type of the attachment in its original form, for example "Microsoft Excel worksheet".

### -field cbEncoding

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">ULONG</a></b>

The size, in bytes, of the value defined by the <b>lpEncoding</b> member.

### -field lpEncoding

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPBYTE</a></b>

Pointer to an X.400 object identifier indicating the form in which the attachment is currently encoded, for example MacBinary, UUENCODE, or binary.

## -remarks

A <b>MapiFileTagExt</b> structure defines the type of an attached file for purposes such as encoding and decoding the file, choosing the correct application to launch when opening it, or any use that requires full information regarding the file type. Client applications can use information in the <b>lpTag</b> and <b>lpEncoding</b> members of this structure to determine what to do with an attachment.

## -see-also

<a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapifiledesc">MapiFileDesc</a>



<a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapifiledescw">MapiFileDescW</a>



<a href="/previous-versions/office/developer/office-2007/cc815513(v=office.12)">PidTagAttachEncoding Canonical Property</a>



<a href="/previous-versions/office/developer/office-2007/cc765770(v=office.12)">PidTagAttachTag Canonical Property</a>

