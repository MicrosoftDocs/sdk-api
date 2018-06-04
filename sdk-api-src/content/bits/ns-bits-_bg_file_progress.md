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
 

 

