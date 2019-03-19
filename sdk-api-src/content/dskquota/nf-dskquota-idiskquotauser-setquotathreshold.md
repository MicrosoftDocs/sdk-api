---
UID: NF:dskquota.IDiskQuotaUser.SetQuotaThreshold
title: IDiskQuotaUser::SetQuotaThreshold (dskquota.h)
author: windows-sdk-content
description: Sets the user's warning threshold value on the volume.
old-location: fs\idiskquotauser_setquotathreshold.htm
tech.root: FileIO
ms.assetid: 7c641a1c-fb04-4039-92bd-d3a1c7045355
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDiskQuotaUser interface [Files],SetQuotaThreshold method, IDiskQuotaUser.SetQuotaThreshold, IDiskQuotaUser::SetQuotaThreshold, SetQuotaThreshold, SetQuotaThreshold method [Files], SetQuotaThreshold method [Files],IDiskQuotaUser interface, _win32_idiskquotauser_setquotathreshold, base.idiskquotauser_setquotathreshold, dskquota/IDiskQuotaUser::SetQuotaThreshold, fs.idiskquotauser_setquotathreshold
ms.topic: method
req.header: dskquota.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Dskquota.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dskquota.dll
api_name:
 - IDiskQuotaUser.SetQuotaThreshold
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiskQuotaUser::SetQuotaThreshold


## -description


Sets the user's warning threshold value on the volume. The threshold is an arbitrary value set by the volume's quota administrator. You can use it to identify users who are approaching their hard quota limit.


## -parameters




### -param llThreshold [in]

The warning threshold value.


### -param fWriteThrough [in]

If this value is <b>TRUE</b>, the value is written immediately to the volume's quota file. Otherwise, the value is written only to the quota user object's local memory. This value should typically be set to <b>TRUE</b>. Set it to <b>FALSE</b> when using the 
<a href="https://msdn.microsoft.com/6cb3da5d-8e4c-45de-b9cf-0f6abf3f1932">IDiskQuotaUserBatch</a> interface to modify multiple user quota entries at the same time.


## -returns



This method returns a file system error or one of the following values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller has insufficient access rights.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_LOCK_FAILED</b></dt>
</dl>
</td>
<td width="60%">
Failure to obtain an exclusive lock.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unexpected file system error occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c1f79e2e-834b-41dc-a15f-6dd1034d021b">Disk Management Interfaces</a>



<a href="https://msdn.microsoft.com/42efbd5b-6455-4319-a76e-cdb666fc36b8">Disk Quotas</a>



<a href="https://msdn.microsoft.com/27edbebc-35b4-4f6a-87cc-d8a99782f405">IDiskQuotaUser</a>
 

 

