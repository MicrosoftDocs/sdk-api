---
UID: NS:bits._BG_FILE_PROGRESS
title: BG_FILE_PROGRESS
author: windows-sdk-content
description: Provides file-related progress information, such as the number of bytes transferred.
old-location: bits\bg_file_progress.htm
tech.root: Bits
ms.assetid: 322363b4-081e-4100-9087-e34c21a3ffae
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BG_FILE_PROGRESS, BG_FILE_PROGRESS structure [BITS], _drz_bg_file_progress, bits.bg_file_progress, bits/BG_FILE_PROGRESS
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
 - BG_FILE_PROGRESS
product: Windows
targetos: Windows
req.typenames: BG_FILE_PROGRESS
req.redist: 
---

# BG_FILE_PROGRESS structure


## -description

Provides file-related progress information, such as the number of bytes transferred.


## -struct-fields




### -field BytesTotal

Size of the file in bytes. If BITS cannot determine the size of the file (for example, if the file or server does not exist), the value is BG_SIZE_UNKNOWN.

If you are downloading ranges from a file, <b>BytesTotal</b> reflects the total number of bytes you want to download from the file.


### -field BytesTransferred

Number of bytes transferred.


### -field Completed

For downloads, the value is <b>TRUE</b> if the file is available to the user; otherwise, the value is <b>FALSE</b>. Files are available to the user after calling the <a href="https://msdn.microsoft.com/d57b0b2e-1181-45ed-b7fc-d002d14527cf">IBackgroundCopyJob::Complete</a> method. If the <b>Complete</b> method generates a  transient error, those files processed before the error occurred are available to the user; the others are not. Use the <b>Completed</b> member to determine if the file is available to the user when 
<b>Complete</b> fails. 




For uploads, the value is <b>TRUE</b> when the file upload is complete; otherwise, the value is <b>FALSE</b>.


## -remarks



To determine if BITS transferred the file, you can:

<ul>
<li>Compare <b>BytesTransferred</b> to <b>BytesTotal</b>.</li>
<li>Implement the <a href="https://msdn.microsoft.com/c7e22911-9c14-48ef-8283-f0787b089432">IBackgroundCopyCallback2::FileTransferred</a> callback.</li>
</ul>
Note that the progress values will be set back to zero if the time stamp of the URL changes.




## -see-also




<a href="https://msdn.microsoft.com/92c5d1d6-1e0b-4b92-9dc5-ec9a4e2c4649">BG_JOB_PROGRESS</a>



<a href="https://msdn.microsoft.com/ea78ee22-87b2-4859-bd49-dd309c8aa234">BG_JOB_REPLY_PROGRESS</a>



<a href="https://msdn.microsoft.com/e72ec5af-7c21-48f8-b027-76a6c9e67f5e">IBackgroundCopyFile::GetProgress</a>



<a href="https://msdn.microsoft.com/b3601f23-1a69-47db-8943-7515652cf015">IBackgroundCopyJob3::AddFileWithRanges</a>
 

 

