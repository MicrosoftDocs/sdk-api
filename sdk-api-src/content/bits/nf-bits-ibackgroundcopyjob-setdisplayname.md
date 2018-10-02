---
UID: NF:bits.IBackgroundCopyJob.SetDisplayName
title: IBackgroundCopyJob::SetDisplayName
author: windows-sdk-content
description: Specifies a display name for the job. Typically, you use the display name to identify the job in a user interface.
old-location: bits\ibackgroundcopyjob_setdisplayname.htm
tech.root: Bits
ms.assetid: 504b0096-891c-4bf7-a311-9d351b359210
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IBackgroundCopyJob interface [BITS],SetDisplayName method, IBackgroundCopyJob.SetDisplayName, IBackgroundCopyJob::SetDisplayName, SetDisplayName, SetDisplayName method [BITS], SetDisplayName method [BITS],IBackgroundCopyJob interface, _drz_ibackgroundcopyjob_setdisplayname, bits.ibackgroundcopyjob_setdisplayname, bits/IBackgroundCopyJob::SetDisplayName
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
 - IBackgroundCopyJob.SetDisplayName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyJob::SetDisplayName


## -description


Specifies a display name for the job. Typically, you use the display name to identify the job in a user interface.


## -parameters




### -param Val

TBD




#### - pDisplayName [in]

Null-terminated string that identifies the job. Must not be <b>NULL</b>. The length of the string is limited to 256 characters, not including the null terminator.


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
Display name was successfully set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pDisplayName</i> parameter cannot be <b>NULL</b> or the name exceeds 256 characters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_STRING_TOO_LONG</b></dt>
</dl>
</td>
<td width="60%">
The display name exceeds 256 characters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.

</td>
</tr>
</table>
 




## -remarks



The display name is originally set when you create the job. For details on specifying the display name when you create the job, see the 
<a href="https://msdn.microsoft.com/6d23e3c0-673b-4f37-b6a0-e364b2d73886">IBackgroundCopyManager::CreateJob</a> method.




## -see-also




<a href="https://msdn.microsoft.com/934cff3e-d4b8-4b76-96e1-fd7ded1842eb">IBackgroundCopyJob::GetDisplayName</a>



<a href="https://msdn.microsoft.com/6d23e3c0-673b-4f37-b6a0-e364b2d73886">IBackgroundCopyManager::CreateJob</a>
 

 

