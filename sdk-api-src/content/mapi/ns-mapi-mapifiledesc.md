---
UID: NS:mapi.MapiFileDesc
title: MapiFileDesc
author: windows-sdk-content
description: A MapiFileDesc structure contains information about a file containing a message attachment stored as a temporary file.
old-location: mapi\mapifiledesc.htm
old-project: windowsmapi
ms.assetid: c2193551-85c3-4293-b632-d6c8ab84800a
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: "*lpMapiFileDesc, MAPI_OLE, MAPI_OLE_STATIC, MapiFileDesc, MapiFileDesc structure, lpMapiFileDesc, lpMapiFileDesc structure pointer, mapi.mapifiledesc, mapi/MapiFileDesc, mapi/lpMapiFileDesc"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: MapiFileDesc, *lpMapiFileDesc
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mapi.h
api_name:
 - MapiFileDesc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MapiFileDesc structure


## -description


A <b>MapiFileDesc</b> structure contains information about a file containing a message attachment stored as a temporary file. That file can contain a static OLE object, an embedded OLE object, an embedded message, and other types of files. For Unicode support, use the <a href="https://msdn.microsoft.com/CF7C41DF-D361-457F-B038-5C1144E70AA6">MapiFileDescW</a> structure.


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

An integer used to indicate where in the message text to render the attachment. Attachments replace the character found at a certain position in the message text. That is, attachments replace the character in the <a href="https://msdn.microsoft.com/7f696dd6-bfae-4c7d-b55f-d37952691c02">MapiMessage</a> structure field <b>NoteText</b>[<b>nPosition</b>]. A value of   -1 (0xFFFFFFFF) means the attachment position is not indicated; the client application will have to provide a way for the user to access the attachment.


### -field lpszPathName

Pointer to the fully qualified path of the attached file. This path should include the disk drive letter and directory name.


### -field lpszFileName

Pointer to the attachment filename seen by the recipient, which may differ from the filename in the <b>lpszPathName</b> member if temporary files are being used. If the <b>lpszFileName</b> member is empty or <b>NULL</b>, the filename from <b>lpszPathName</b> is used.


### -field lpFileType

Pointer to the attachment file type, which can be represented with a <a href="https://msdn.microsoft.com/5f6de637-14a8-46bb-a53e-f355d7592222">MapiFileTagExt</a> structure. A value of <b>NULL</b> indicates an unknown file type or a file type determined by the operating system.


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

OLE object files are file representations of OLE object streams. The client application can re-create an OLE object from the file by calling the OLE function <a href="https://msdn.microsoft.com/2d54a0ef-906b-4886-a095-4ff2f3d4e634">OleLoadFromStream</a> with an OLESTREAM object that reads the file contents. If an OLE file attachment is included in an outbound message, the OLE object stream should be written directly to the file used as the attachment. 

When using the <b>MapiFileDesc</b> member <b>nPosition</b>, the client application should not place two attachments in the same location. Client applications might not display file attachments at positions beyond the end of the message text. 




## -see-also




<a href="https://msdn.microsoft.com/CF7C41DF-D361-457F-B038-5C1144E70AA6">MapiFileDescW</a>



<a href="https://msdn.microsoft.com/7f696dd6-bfae-4c7d-b55f-d37952691c02">MapiMessage</a>



<a href="https://msdn.microsoft.com/3C74A9C0-1483-4A97-94EB-19A0D30D9A08">MapiMessageW</a>
 

 

