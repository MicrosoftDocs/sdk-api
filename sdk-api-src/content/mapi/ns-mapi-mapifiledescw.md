---
UID: NS:mapi.MapiFileDescW
title: MapiFileDescW (mapi.h)
description: A MapiFileDescW structure contains information about a file containing a message attachment stored as a temporary file. That file can contain a static OLE object, an embedded OLE object, an embedded message, and other types of files.
helpviewer_keywords: ["*lpMapiFileDescW","MAPI_OLE","MAPI_OLE_STATIC","MapiFileDescW","MapiFileDescW structure","lpMapiFileDescW","lpMapiFileDescW structure pointer","mapi.mapifiledescw","mapi/MapiFileDescW","mapi/lpMapiFileDescW"]
old-location: mapi\mapifiledescw.htm
tech.root: mapi
ms.assetid: CF7C41DF-D361-457F-B038-5C1144E70AA6
ms.date: 12/05/2018
ms.keywords: '*lpMapiFileDescW, MAPI_OLE, MAPI_OLE_STATIC, MapiFileDescW, MapiFileDescW structure, lpMapiFileDescW, lpMapiFileDescW structure pointer, mapi.mapifiledescw, mapi/MapiFileDescW, mapi/lpMapiFileDescW'
req.header: mapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: MapiFileDescW, *lpMapiFileDescW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lpMapiFileDescW
 - mapi/lpMapiFileDescW
 - MapiFileDescW
 - mapi/MapiFileDescW
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
 - MapiFileDescW
---

# MapiFileDescW structure


## -description

A <b>MapiFileDescW</b> structure contains information about a file containing a message attachment stored as a temporary file. That file can contain a static OLE object, an embedded OLE object, an embedded message, and other types of files.

## -struct-fields

### -field ulReserved

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">ULONG</a></b>

Reserved; must be 0.

### -field flFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">ULONG</a></b>

Bitmask of attachment flags. The following flags can be set.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MAPI_OLE"></a><a id="mapi_ole"></a><dl>
<dt><b>MAPI_OLE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The attachment is an OLE object. If <b>MAPI_OLE_STATIC</b> is also set, the attachment is a static OLE object. If <b>MAPI_OLE_STATIC</b> is not set, the attachment is an embedded OLE object.

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_OLE_STATIC"></a><a id="mapi_ole_static"></a><dl>
<dt><b>MAPI_OLE_STATIC</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The attachment is a static OLE object.

</td>
</tr>
</table>
 

If neither flag is set, the attachment is treated as a data file.

### -field nPosition

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">ULONG</a></b>

An integer used to indicate where the attachment is rendered in the message text. The message text is stored in the <b>NoteText</b> member of the <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessagew">MapiMessageW</a> structure, and the integer is used as an index to identify a specific character in the message string, <b>NoteText</b>[<b>nPosition</b>], that is replaced by the attachment.

A value of   -1 (0xFFFFFFFF) means the attachment position is not indicated and the client application must provide a way for the user to access the attachment.

### -field lpszPathName

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">PWSTR</a></b>

Pointer to the fully qualified path of the attached file. This path should include the disk drive letter and directory name.

### -field lpszFileName

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">PWSTR</a></b>

Pointer to the filename of the attachment as seen by the recipient. The filename that is seen by the recipient may differ from the filename in the <b>lpszPathName</b> member if temporary files are being used.

If the <b>lpszFileName</b> member is empty or <b>NULL</b>, the filename from <b>lpszPathName</b> is used.

### -field lpFileType

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">PVOID</a></b>

Pointer to the attachment file type, which can be represented with a <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapifiletagext">MapiFileTagExt</a> structure.

A value of <b>NULL</b> indicates an unknown file type or a file type determined by the operating system.

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
Data file attachments are simply data files. OLE object file attachments are OLE objects that are displayed in the message text. If the OLE attachment is editable, the recipient can double-click it and its source application will be started to handle the edit session. If the OLE attachment is static, the object cannot be edited. The flag set in the <b>flFlags</b> member of the <b>MapiFileDescW</b> structure determines the kind of a particular attachment. Embedded messages can be identified by a .MSG extension in the <b>lpszFileName</b> member.

OLE object files are file representations of OLE object streams. The client application can re-create an OLE object from the file by calling the OLE function <a href="/windows/desktop/api/ole/nf-ole-oleloadfromstream">OleLoadFromStream</a> with an OLESTREAM object that reads the file contents. If an OLE file attachment is included in an outbound message, the OLE object stream should be written directly to the file used as the attachment. 

When using the <b>MapiFileDescW</b> member <b>nPosition</b>, the client application should not place two attachments in the same location. Client applications might not display file attachments at positions beyond the end of the message text.

## -see-also

<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmailw">MAPISendMailW</a>



<a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapifiledesc">MapiFileDesc</a>



<a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessagew">MapiMessageW</a>

