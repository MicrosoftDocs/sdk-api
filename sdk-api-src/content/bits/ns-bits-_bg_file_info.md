---
UID: NS:bits._BG_FILE_INFO
title: "_BG_FILE_INFO"
author: windows-sdk-content
description: The BG_FILE_INFO structure provides the local and remote names of the file to transfer.
old-location: bits\bg_file_info.htm
tech.root: Bits
ms.assetid: bf5302e9-da8f-4c57-a998-fd49484e0584
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: BG_FILE_INFO, BG_FILE_INFO structure [BITS], _BG_FILE_INFO, _drz_bg_file_info, bits.bg_file_info, bits/BG_FILE_INFO
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
 - Bits.h
api_name:
 - BG_FILE_INFO
product: Windows
targetos: Windows
req.typenames: BG_FILE_INFO
req.redist: 
---

# _BG_FILE_INFO structure


## -description


The 
<b>BG_FILE_INFO</b> structure provides the local and remote names of the file to transfer.


## -struct-fields




### -field RemoteName

Null-terminated string that contains the name of the file on the server (for example, http://&lt;server&gt;/&lt;path&gt;/file.ext). The format of the name must conform to the transfer protocol you use. You cannot use wildcards in the path or file name. The URL must  contain only legal URL characters; no escape processing is performed. The URL is limited to 2,200 characters, not including the null terminator. 


Each segment of the URL is limited to MAX_PATH characters.

You can use SMB to express the remote name of the file to download or upload; there is no SMB support for  upload-reply jobs. You can specify the remote name as a UNC path, full path with a network drive, or use the "file://" prefix. <b>BITS 1.5 and earlier:  </b>The SMB protocol for <b>RemoteName</b> is not supported.




### -field LocalName

Null-terminated string that contains the name of the file on the client. The file name must include the full path  (for example, d:\myapp\updates\file.ext). You cannot use wildcards in the path or file name, and directories in the path must exist. The path is limited to MAX_PATH, not including the null terminator. 

The user must have permission to write to the local directory for downloads and the reply portion of an upload-reply job. BITS does not support NTFS streams. Instead of using network drives, which are session specific, use UNC paths (for example, \\server\share\path\file). Do not include the \\? prefix in the path.


## -remarks



BITS supports the HTTP, HTTPS, and SMB protocols for <b>RemoteName</b>. For HTTP requirements, see <a href="https://msdn.microsoft.com/35af422b-62e4-41fd-8890-579ccf016c83">HTTP Requirements for BITS Downloads</a>.

<b>BITS 1.5 and earlier:  </b>The SMB protocol for <b>RemoteName</b> is not supported.

The following identifies whether BITS propagates a file's time stamps:

<ul>
<li>For HTTP downloads, BITS propagates the file's modification time stamp and sets the file's creation time to the modification time.</li>
<li>For HTTP uploads, BITS does not propagate the file's time stamps.</li>
<li>For SMB downloads and uploads, BITS propagates the file's time stamps.</li>
</ul>
BITS does not support SMB paths to named pipes or devices.  To maintain the owner and ACL information for files downloaded using SMB, call the <a href="https://msdn.microsoft.com/de218e3d-8c42-4cf3-94b9-94dbc5edbb47">IBackgroundCopyJob3::SetFileACLFlags</a> method.

If the path and file name portion of the URL for an HTTP upload and upload-reply job contains Unicode characters not in common to the code page on both the client and server, the URL translation will fail on the server and the BITS job will be placed in the error state.
If the server portion of the URL contains Unicode characters, you must encode the server portion using <a href="http://go.microsoft.com/fwlink/p/?linkid=166153">Internationalized Domain Names</a> (IDN).

BITS does not limit the size of file you can download using HTTP. For upload limits, see the <a href="https://msdn.microsoft.com/08a40cc1-ec6d-4b65-971a-15c7b06df148">BITSMaximumUploadSize</a> 
IIS extension property. 

<b>IIS 5.0:  </b>Downloads are limited to 4 GB.

<b>BITS 1.2 and earlier:  </b>For HTTP downloads, the maximum file size you can transfer is 4 GB; BITS cannot guarantee the successful transfer of files over 4 GB. If the  URL contains Unicode characters that are not in the US-ASCII character set, encode the Unicode string in UTF-8 before passing it as the remote file name to BITS. If you do not encode the string, the HTTP server may receive an incorrect URL and the job may enter the error state.






## -see-also




<a href="https://msdn.microsoft.com/6dd33b7d-4317-4eb5-aae4-83d3f4416bf9">IBackgroundCopyFile2::SetRemoteName</a>



<a href="https://msdn.microsoft.com/d27844b7-a5c6-4f4c-a1db-80e031898634">IBackgroundCopyFile::GetLocalName</a>



<a href="https://msdn.microsoft.com/b6b1b1dc-776e-4369-bd39-d159e4edfe38">IBackgroundCopyFile::GetRemoteName</a>



<a href="https://msdn.microsoft.com/5ea62d29-c40e-4bd2-b22a-fce2d9f4eecf">IBackgroundCopyJob3::ReplaceRemotePrefix</a>



<a href="https://msdn.microsoft.com/fe2f9b47-0f0a-48ab-be0e-658307cfec5f">IBackgroundCopyJob::AddFileSet</a>
 

 

