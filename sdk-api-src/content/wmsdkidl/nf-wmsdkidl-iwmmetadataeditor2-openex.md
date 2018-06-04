---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IWMMetadataEditor2::OpenEx


## -description



The <b>OpenEx</b> method opens a file for use by the metadata editor object. <b>OpenEx</b> opens ASF files and MP3 files, though the metadata editor has limited capabilities when working with MP3 files.




## -parameters




### -param pwszFilename [in]

Pointer to a wide-character null-terminated string containing the file name.


### -param dwDesiredAccess [in]

<b>DWORD</b> containing the desired access type. This can be set to GENERIC_READ or GENERIC_WRITE. For read/write access, pass both values combined with a bitwise <b>OR</b>. When using GENERIC_READ, you must also pass a valid sharing mode as <i>dwShareMode</i>. Failure to do so will result in an error.


### -param dwShareMode [in]

<b>DWORD</b> containing the sharing mode. This can be one of the values in the following table or a combination of the two using a bitwise <b>OR</b>. A value of zero indicates no sharing. Sharing is not supported when requesting read/write access. If you request read/write access and pass any value other than zero for the share mode, an error is returned.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>FILE_SHARE_READ</td>
<td>Subsequent open operations on the file will succeed only if read access is requested.</td>
</tr>
<tr>
<td>FILE_SHARE_DELETE</td>
<td>(NTFS only) Subsequent open operations on the file will succeed only if it is being deleted.</td>
</tr>
</table>
 


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Read/write access has been requested using file sharing.

OR

Read access has been requested without indicating read-and-delete file sharing.

OR

The access mode requested is not available with this method.

</td>
</tr>
</table>
 




## -remarks



The parameters <i>dwDesiredAccess</i> and <i>dwShareMode</i> are identical to those used in the <b>OpenFile</b> function defined in the Platform SDK. In the case of <b>OpenEx</b>, however, only a limited set of values are valid for <i>dwDesiredAccess</i>. Using any value other than those specified will result in an error.




## -see-also




<a href="https://msdn.microsoft.com/e991ac8e-35af-484f-8c60-dc6a7d402120">IWMMetadataEditor2 Interface</a>



<a href="https://msdn.microsoft.com/01dd09ff-35d2-4e00-9eab-5110a426449f">IWMMetadataEditor::Open</a>
 

 

