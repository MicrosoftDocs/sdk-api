---
UID: NF:dskquota.IDiskQuotaUser.GetSid
title: IDiskQuotaUser::GetSid
author: windows-sdk-content
description: Retrieves the user's security identifier (SID).
old-location: fs\idiskquotauser_getsid.htm
tech.root: FileIO
ms.assetid: 1718b5eb-2385-4e0f-a6af-99a5ef73e55d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSid, GetSid method [Files], GetSid method [Files],IDiskQuotaUser interface, IDiskQuotaUser interface [Files],GetSid method, IDiskQuotaUser.GetSid, IDiskQuotaUser::GetSid, _win32_idiskquotauser_getsid, base.idiskquotauser_getsid, dskquota/IDiskQuotaUser::GetSid, fs.idiskquotauser_getsid
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
 - IDiskQuotaUser.GetSid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiskQuotaUser::GetSid


## -description


Retrieves the user's security identifier (SID).


## -parameters




### -param pbSidBuffer [out]

The SID.


### -param cbSidBuffer [in]

The size of the buffer, in bytes. Use the 
<a href="https://msdn.microsoft.com/68fcb122-5d61-464a-99ae-d99e0d4a8117">IDiskQuotaUser::GetSidLength</a> method to obtain the required size for the buffer.


## -returns



This method returns one of the following values.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pbSidBuffer</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SID</b></dt>
</dl>
</td>
<td width="60%">
The SID for the user is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Insufficient destination buffer size.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c1f79e2e-834b-41dc-a15f-6dd1034d021b">Disk Management Interfaces</a>



<a href="https://msdn.microsoft.com/42efbd5b-6455-4319-a76e-cdb666fc36b8">Disk Quotas</a>



<a href="https://msdn.microsoft.com/27edbebc-35b4-4f6a-87cc-d8a99782f405">IDiskQuotaUser</a>
 

 

