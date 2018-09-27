---
UID: NF:dskquota.IDiskQuotaUser.GetQuotaLimitText
title: IDiskQuotaUser::GetQuotaLimitText
author: windows-sdk-content
description: Retrieves the user's quota limit for the volume.
old-location: fs\idiskquotauser_getquotalimittext.htm
tech.root: fileio
ms.assetid: 2c200aae-dbc5-487c-a3a4-e8dcf50bc0f9
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetQuotaLimitText, GetQuotaLimitText method [Files], GetQuotaLimitText method [Files],IDiskQuotaUser interface, IDiskQuotaUser interface [Files],GetQuotaLimitText method, IDiskQuotaUser.GetQuotaLimitText, IDiskQuotaUser::GetQuotaLimitText, _win32_idiskquotauser_getquotalimittext, base.idiskquotauser_getquotalimittext, dskquota/IDiskQuotaUser::GetQuotaLimitText, fs.idiskquotauser_getquotalimittext
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
 - IDiskQuotaUser.GetQuotaLimitText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiskQuotaUser::GetQuotaLimitText


## -description


Retrieves the user's quota limit for the volume. This limit is expressed as a text string, for example "10.5 MB". If the user has no quota limit, the string returned is "No Limit" (localized). If the destination buffer is too small, the string is truncated to fit the buffer.


## -parameters




### -param pszText [out]

The text string.


### -param cchText [in]

The size of the buffer, in characters.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pszText</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected exception occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c1f79e2e-834b-41dc-a15f-6dd1034d021b">Disk Management Interfaces</a>



<a href="https://msdn.microsoft.com/42efbd5b-6455-4319-a76e-cdb666fc36b8">Disk Quotas</a>



<a href="https://msdn.microsoft.com/27edbebc-35b4-4f6a-87cc-d8a99782f405">IDiskQuotaUser</a>
 

 

