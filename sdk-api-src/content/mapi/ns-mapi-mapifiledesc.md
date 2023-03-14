---
UID: NS:mapi.MapiFileDesc
title: MapiFileDesc (mapi.h)
description: A MapiFileDesc structure contains information about a file containing a message attachment stored as a temporary file.
helpviewer_keywords: ["*lpMapiFileDesc","MAPI_OLE","MAPI_OLE_STATIC","MapiFileDesc","MapiFileDesc structure","lpMapiFileDesc","lpMapiFileDesc structure pointer","mapi.mapifiledesc","mapi/MapiFileDesc","mapi/lpMapiFileDesc"]
old-location: mapi\mapifiledesc.htm
tech.root: mapi
ms.assetid: c2193551-85c3-4293-b632-d6c8ab84800a
ms.date: 12/05/2018
ms.keywords: '*lpMapiFileDesc, MAPI_OLE, MAPI_OLE_STATIC, MapiFileDesc, MapiFileDesc structure, lpMapiFileDesc, lpMapiFileDesc structure pointer, mapi.mapifiledesc, mapi/MapiFileDesc, mapi/lpMapiFileDesc'
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
req.typenames: MapiFileDesc, *lpMapiFileDesc
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lpMapiFileDesc
 - mapi/lpMapiFileDesc
 - MapiFileDesc
 - mapi/MapiFileDesc
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
 - MapiFileDesc
---

# MapiFileDesc structure


## -description

A <b>MapiFileDesc</b> structure contains information about a file containing a message attachment stored as a temporary file. That file can contain a static OLE object, an embedded OLE object, an embedded message, and other types of files. For Unicode support, use the <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapifiledescw">MapiFileDescW</a> structure.

## -struct-fields

### -field ulReserved

Reserved; must be zero.

### -field flFlags

Bitmask of option flags. The following flags can be set.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MAPI_OLE"></a><a id="mapi_ole"></a><dl>
<dt><b>MAPI_OLE</b></dt>
</dl>
</td>
<td width="60%">
The attachment is an OLE object. If MAPI_OLE_STATIC is also set, the attachment is a static OLE object. If MAPI_OLE_STATIC is not set, the attachment is an embedded OLE object.

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_OLE_STATIC"></a><a id="mapi_ole_static"></a><dl>
<dt><b>MAPI_OLE_STATIC</b></dt>
</dl>
</td>
<td width="60%">
The attachment is a static OLE object.

</td>
</tr>
</table>
 

If neither flag is set, the attachment is treated as a data file.

### -field nPosition

An integer used to indicate where in the message text to render the attachment. Attachments replace the character found at a certain position in the message text. That is, attachments replace the character in the <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessage">MapiMessage</a> structure field <b>NoteText</b>[<b>nPosition</b>]. A value of   -1 (0xFFFFFFFF) means the attachment position is not indicated; the client application will have to provide a way for the user to access the attachment.

### -field lpszPathName

Pointer to the fully qualified path of the attached file. This path should include the disk drive letter and directory name.

### -field lpszFileName

Pointer to the attachment filename seen by the recipient, which may differ from the filename in the <b>lpszPathName</b> member if temporary files are being used. If the <b>lpszFileName</b> member is empty or <b>NULL</b>, the filename from <b>lpszPathName</b> is used.

### -field lpFileType

Pointer to the attachment file type, which can be represented with a <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapifiletagext">MapiFileTagExt</a> structure. A value of <b>NULL</b> indicates an unknown file type or a file type determined by the operating system.

## -remarks

Simple MAPI works with three kinds of embedded attachments:  

<ul>
<li>
Data file attachments

</li>
<li>
Editable OLE object file attachments

</li>
<li>
Static OLE object file attachments

</li>
</ul>
Data file attachments are simply data files. OLE object file attachments are OLE objects that are displayed in the message text. If the OLE attachment is editable, the recipient can double-click it and its source application will be started to handle the edit session. If the OLE attachment is static, the object cannot be edited. The flag set in the <b>flFlags</b> member of the <b>MapiFileDesc</b> structure determines the kind of a particular attachment. Embedded messages can be identified by a .MSG extension in the <b>lpszFileName</b> member.

OLE object files are file representations of OLE object streams. The client application can re-create an OLE object from the file by calling the OLE function <a href="/windows/desktop/api/ole/nf-ole-oleloadfromstream">OleLoadFromStream</a> with an OLESTREAM object that reads the file contents. If an OLE file attachment is included in an outbound message, the OLE object stream should be written directly to the file used as the attachment. 

When using the <b>MapiFileDesc</b> member <b>nPosition</b>, the client application should not place two attachments in the same location. Client applications might not display file attachments at positions beyond the end of the message text.

## -see-also

<a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapifiledescw">MapiFileDescW</a>



<a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessage">MapiMessage</a>



<a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessagew">MapiMessageW</a>

