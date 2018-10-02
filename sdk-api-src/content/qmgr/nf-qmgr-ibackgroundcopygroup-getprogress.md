---
UID: NF:qmgr.IBackgroundCopyGroup.GetProgress
title: IBackgroundCopyGroup::GetProgress
author: windows-sdk-content
description: Use the GetProgress method to retrieve the progress of the download.
old-location: bits\ibackgroundcopygroup_getprogress.htm
tech.root: Bits
ms.assetid: a596a005-a3ad-4d2b-b19b-60c2279590da
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetProgress, GetProgress method [BITS], GetProgress method [BITS],IBackgroundCopyGroup interface, IBackgroundCopyGroup interface [BITS],GetProgress method, IBackgroundCopyGroup.GetProgress, IBackgroundCopyGroup::GetProgress, QM_PROGRESS_PERCENT_DONE, QM_PROGRESS_SIZE_DONE, QM_PROGRESS_TIME_DONE, bits.ibackgroundcopygroup_getprogress, qmgr/IBackgroundCopyGroup::GetProgress
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: qmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Qmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
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
 - IBackgroundCopyGroup.GetProgress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyGroup::GetProgress


## -description


<p class="CCE_Message">[<b>IBackgroundCopyGroup</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/72668c9b-e6f3-4f3f-9d4b-50d930d1889d">BITS interfaces</a>.]

Use the <b>GetProgress</b> method to retrieve the progress of the download.


## -parameters




### -param dwFlags [in]

Type of progress to retrieve. Specify one of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="QM_PROGRESS_PERCENT_DONE"></a><a id="qm_progress_percent_done"></a><dl>
<dt><b>QM_PROGRESS_PERCENT_DONE</b></dt>
</dl>
</td>
<td width="60%">
Returns the percent of the download that is complete.

</td>
</tr>
<tr>
<td width="40%"><a id="QM_PROGRESS_SIZE_DONE"></a><a id="qm_progress_size_done"></a><dl>
<dt><b>QM_PROGRESS_SIZE_DONE</b></dt>
</dl>
</td>
<td width="60%">
Returns the number of bytes downloaded.

</td>
</tr>
<tr>
<td width="40%"><a id="QM_PROGRESS_TIME_DONE"></a><a id="qm_progress_time_done"></a><dl>
<dt><b>QM_PROGRESS_TIME_DONE</b></dt>
</dl>
</td>
<td width="60%">
Not supported.

</td>
</tr>
</table>
 


### -param pdwProgress [out]

Progress of the download. The progress represents the number of bytes downloaded or the percent of the download that is complete, depending on <i>dwFlags</i>. 


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
Successfully retrieved the group's progress.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
You cannot specify QM_PROGRESS_TIME_DONE for the <i>dwFlags</i> parameter.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/51ddd89a-489a-4b83-ad45-838809a6d2e8">IBackgroundCopyGroup</a>
 

 

