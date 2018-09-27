---
UID: NS:bits._BG_FILE_PROGRESS
title: "_BG_FILE_PROGRESS"
author: windows-sdk-content
description: The BG_FILE_PROGRESS structure provides file-related progress information, such as the number of bytes transferred.
old-location: bits\bg_file_progress.htm
tech.root: Bits
ms.assetid: 322363b4-081e-4100-9087-e34c21a3ffae
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: BG_FILE_PROGRESS, BG_FILE_PROGRESS structure [BITS], _BG_FILE_PROGRESS, _drz_bg_file_progress, bits.bg_file_progress, bits/BG_FILE_PROGRESS
ms.prod: windows
ms.technology: windows-sdk
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

# _BG_FILE_PROGRESS structure


## -description


The 
<b>BG_FILE_PROGRESS</b> structure provides file-related progress information, such as the number of bytes transferred.


## -struct-fields




### -field BytesTotal

Size of the file in bytes. If BITS cannot determine the size of the file (for example, if the file or server does not exist), the value is BG_SIZE_UNKNOWN.

If you are downloading ranges from a file, <b>BytesTotal</b> reflects the total number of bytes you want to download from the file.


### -field BytesTransferred

Number of bytes transferred.


### -field Completed

For downloads, the value is <b>TRUE</b> if the file is available to the user; otherwise, the value is <b>FALSE</b>. Files are available to the user after calling the <a href="https://msdn.microsoft.com/en-us/library/Aa363021(v=VS.85).aspx">IBackgroundCopyJob::Complete</a> method. If the <b>Complete</b> method generates a  transient error, those files processed before the error occurred are available to the user; the others are not. Use the <b>Completed</b> member to determine if the file is available to the user when 
<b>Complete</b> fails. 




For uploads, the value is <b>TRUE</b> when the file upload is complete; otherwise, the value is <b>FALSE</b>.


## -remarks



To determine if BITS transferred the file, you can:

<ul>
<li>Compare <b>BytesTransferred</b> to <b>BytesTotal</b>.</li>
<li>Implement the <a href="https://msdn.microsoft.com/en-us/library/Aa362871(v=VS.85).aspx">IBackgroundCopyCallback2::FileTransferred</a> callback.</li>
</ul>
Note that the progress values will be set back to zero if the time stamp of the URL changes.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362806(v=VS.85).aspx">BG_JOB_PROGRESS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362808(v=VS.85).aspx">BG_JOB_REPLY_PROGRESS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362957(v=VS.85).aspx">IBackgroundCopyFile::GetProgress</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362991(v=VS.85).aspx">IBackgroundCopyJob3::AddFileWithRanges</a>
 

 

