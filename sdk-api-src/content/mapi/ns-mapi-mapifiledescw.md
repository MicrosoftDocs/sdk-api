---
UID: NS:mapi.__unnamed_struct_1
title: MapiFileDescW (mapi.h)
author: windows-sdk-content
description: A MapiFileDescW structure contains information about a file containing a message attachment stored as a temporary file. That file can contain a static OLE object, an embedded OLE object, an embedded message, and other types of files.
old-location: mapi\mapifiledescw.htm
tech.root: WindowsMAPI
ms.assetid: CF7C41DF-D361-457F-B038-5C1144E70AA6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*lpMapiFileDescW, MAPI_OLE, MAPI_OLE_STATIC, MapiFileDescW, MapiFileDescW structure, lpMapiFileDescW, lpMapiFileDescW structure pointer, mapi.mapifiledescw, mapi/MapiFileDescW, mapi/lpMapiFileDescW"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mapi.h
api_name:
 - MapiFileDescW
product: Windows
targetos: Windows
req.typenames: MapiFileDescW, *lpMapiFileDescW
req.redist: 
---

# MapiFileDescW structure


## -description


A <b>MapiFileDescW</b> structure contains information about a file containing a message attachment stored as a temporary file. That file can contain a static OLE object, an embedded OLE object, an embedded message, and other types of files.


## -struct-fields




### -field ulReserved

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">ULONG</a></b>

Reserved; must be 0.


### -field flFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">ULONG</a></b>

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

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">ULONG</a></b>

An integer used to indicate where the attachment is rendered in the message text. The message text is stored in the <b>NoteText</b> member of the <a href="https://msdn.microsoft.com/3C74A9C0-1483-4A97-94EB-19A0D30D9A08">MapiMessageW</a> structure, and the integer is used as an index to identify a specific character in the message string, <b>NoteText</b>[<b>nPosition</b>], that is replaced by the attachment.

A value of   -1 (0xFFFFFFFF) means the attachment position is not indicated and the client application must provide a way for the user to access the attachment.


### -field lpszPathName

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">PWSTR</a></b>

Pointer to the fully qualified path of the attached file. This path should include the disk drive letter and directory name.


### -field lpszFileName

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">PWSTR</a></b>

Pointer to the filename of the attachment as seen by the recipient. The filename that is seen by the recipient may differ from the filename in the <b>lpszPathName</b> member if temporary files are being used.

If the <b>lpszFileName</b> member is empty or <b>NULL</b>, the filename from <b>lpszPathName</b> is used.


### -field lpFileType

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">PVOID</a></b>

Pointer to the attachment file type, which can be represented with a <a href="https://msdn.microsoft.com/5f6de637-14a8-46bb-a53e-f355d7592222">MapiFileTagExt</a> structure.

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

OLE object files are file representations of OLE object streams. The client application can re-create an OLE object from the file by calling the OLE function <a href="https://msdn.microsoft.com/2d54a0ef-906b-4886-a095-4ff2f3d4e634">OleLoadFromStream</a> with an OLESTREAM object that reads the file contents. If an OLE file attachment is included in an outbound message, the OLE object stream should be written directly to the file used as the attachment. 

When using the <b>MapiFileDescW</b> member <b>nPosition</b>, the client application should not place two attachments in the same location. Client applications might not display file attachments at positions beyond the end of the message text. 




## -see-also




<a href="https://msdn.microsoft.com/FA6FB49A-FA13-4F2F-8B89-5FD38B18B41B">MAPISendMailW</a>



<a href="https://msdn.microsoft.com/c2193551-85c3-4293-b632-d6c8ab84800a">MapiFileDesc</a>



<a href="https://msdn.microsoft.com/3C74A9C0-1483-4A97-94EB-19A0D30D9A08">MapiMessageW</a>
 

 

