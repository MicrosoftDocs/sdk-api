---
UID: NF:bits.IBackgroundCopyJob.GetDisplayName
title: IBackgroundCopyJob::GetDisplayName
author: windows-sdk-content
description: Retrieves the display name for the job. Typically, you use the display name to identify the job in a user interface.
old-location: bits\ibackgroundcopyjob_getdisplayname.htm
old-project: Bits
ms.assetid: 934cff3e-d4b8-4b76-96e1-fd7ded1842eb
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: GetDisplayName, GetDisplayName method [BITS], GetDisplayName method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],GetDisplayName method, IBackgroundCopyJob.GetDisplayName, IBackgroundCopyJob::GetDisplayName, _drz_ibackgroundcopyjob_getdisplayname, bits.ibackgroundcopyjob_getdisplayname, bits/IBackgroundCopyJob::GetDisplayName
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BG_JOB_PROXY_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyJob.GetDisplayName
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
---

# IBackgroundCopyJob::GetDisplayName


## -description


Retrieves the display name for the job. Typically, you use the display name to identify the job in a user interface.


## -parameters




### -param pVal






#### - ppDisplayName [out]

Null-terminated string that contains the display name that identifies the job. More than one job can have the same display name. Call the 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function to free <i>ppDisplayName</i> when done.


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
Display name was successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppDisplayName</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/504b0096-891c-4bf7-a311-9d351b359210">IBackgroundCopyJob::SetDisplayName</a>
 

 

