---
UID: NF:bits3_0.IBackgroundCopyJob4.GetMaximumDownloadTime
title: IBackgroundCopyJob4::GetMaximumDownloadTime (bits3_0.h)
author: windows-sdk-content
description: Retrieves the maximum time that BITS will spend transferring the files in the job.
old-location: bits\ibackgroundcopyjob4_getmaximumdownloadtime.htm
tech.root: Bits
ms.assetid: 2d258dc4-a6fd-46d7-ac90-2703c8ddc666
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetMaximumDownloadTime, GetMaximumDownloadTime method [BITS], GetMaximumDownloadTime method [BITS],IBackgroundCopyJob4 interface, IBackgroundCopyJob4 interface [BITS],GetMaximumDownloadTime method, IBackgroundCopyJob4.GetMaximumDownloadTime, IBackgroundCopyJob4::GetMaximumDownloadTime, bits.ibackgroundcopyjob4_getmaximumdownloadtime, bits3_0/IBackgroundCopyJob4::GetMaximumDownloadTime
ms.topic: method
req.header: bits3_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyJob4.GetMaximumDownloadTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyJob4::GetMaximumDownloadTime


## -description


Retrieves the maximum time that BITS will spend transferring the files in the job.


## -parameters




### -param pTimeout [out]

Maximum time, in seconds, that BITS will spend transferring the files in the job.


## -returns



The method returns the following return values.

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
Success

</td>
</tr>
</table>
 




## -remarks



The value is the maximum elapsed time that the job can spend in the CONNECTING or TRANSFERRING state. Time spent in the QUEUED or TRANSIENT_ERROR state does not count against the timeout value.




## -see-also




<a href="https://msdn.microsoft.com/68909710-f749-487e-b064-9f8630929c53">IBackgroundCopyJob4</a>



<a href="https://msdn.microsoft.com/9e29c082-5bd1-465a-8853-aea81a593db6">IBackgroundCopyJob4::SetMaximumDownloadTime</a>
 

 

