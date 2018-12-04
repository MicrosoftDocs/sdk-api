---
UID: NF:bits.IBackgroundCopyJob.GetProgress
title: IBackgroundCopyJob::GetProgress
author: windows-sdk-content
description: Retrieves job-related progress information, such as the number of bytes and files transferred.
old-location: bits\ibackgroundcopyjob_getprogress.htm
tech.root: bits
ms.assetid: 30aae990-1cc1-468b-9e5f-7ef5ce6eeb9a
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetProgress, GetProgress method [BITS], GetProgress method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],GetProgress method, IBackgroundCopyJob.GetProgress, IBackgroundCopyJob::GetProgress, _drz_ibackgroundcopyjob_getprogress, bits.ibackgroundcopyjob_getprogress, bits/IBackgroundCopyJob::GetProgress
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyJob.GetProgress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyJob::GetProgress


## -description


Retrieves job-related progress information, such as the number of bytes and files transferred. 


## -parameters




### -param pVal [out]

Contains data that you can use to calculate the percentage of the job that is complete. For more information, see 
<a href="https://msdn.microsoft.com/92c5d1d6-1e0b-4b92-9dc5-ec9a4e2c4649">BG_JOB_PROGRESS</a>.


## -returns



This method returns the following <b>HRESULT</b> values, as well as others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Progress information was successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pProgress</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/92c5d1d6-1e0b-4b92-9dc5-ec9a4e2c4649">BG_JOB_PROGRESS</a>
 

 

