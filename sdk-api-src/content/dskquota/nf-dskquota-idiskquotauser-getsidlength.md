---
UID: NF:dskquota.IDiskQuotaUser.GetSidLength
title: IDiskQuotaUser::GetSidLength
author: windows-sdk-content
description: Retrieves the length of the user's security identifier (SID), in bytes.
old-location: fs\idiskquotauser_getsidlength.htm
tech.root: fileio
ms.assetid: 68fcb122-5d61-464a-99ae-d99e0d4a8117
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: GetSidLength, GetSidLength method [Files], GetSidLength method [Files],IDiskQuotaUser interface, IDiskQuotaUser interface [Files],GetSidLength method, IDiskQuotaUser.GetSidLength, IDiskQuotaUser::GetSidLength, _win32_idiskquotauser_getsidlength, base.idiskquotauser_getsidlength, dskquota/IDiskQuotaUser::GetSidLength, fs.idiskquotauser_getsidlength
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDiskQuotaUser.GetSidLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiskQuotaUser::GetSidLength


## -description


Retrieves the length of the user's security identifier (SID), in bytes. Use the return value to determine the size of the destination buffer you pass to 
<a href="https://msdn.microsoft.com/1718b5eb-2385-4e0f-a6af-99a5ef73e55d">IDiskQuotaUser::GetSid</a>.


## -parameters




### -param pdwLength [out]

The SID length, in bytes.


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
The <i>pdwLength</i> parameter is <b>NULL</b>.

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
 

 

