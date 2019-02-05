---
UID: NF:dskquota.IDiskQuotaUser.GetQuotaThresholdText
title: IDiskQuotaUser::GetQuotaThresholdText
author: windows-sdk-content
description: Retrieves the user's warning threshold for the volume.
old-location: fs\idiskquotauser_getquotathresholdtext.htm
tech.root: FileIO
ms.assetid: 19391a9e-e64c-4e6f-8b52-efe59ed45ae5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetQuotaThresholdText, GetQuotaThresholdText method [Files], GetQuotaThresholdText method [Files],IDiskQuotaUser interface, IDiskQuotaUser interface [Files],GetQuotaThresholdText method, IDiskQuotaUser.GetQuotaThresholdText, IDiskQuotaUser::GetQuotaThresholdText, _win32_idiskquotauser_getquotathresholdtext, base.idiskquotauser_getquotathresholdtext, dskquota/IDiskQuotaUser::GetQuotaThresholdText, fs.idiskquotauser_getquotathresholdtext
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
 - IDiskQuotaUser.GetQuotaThresholdText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiskQuotaUser::GetQuotaThresholdText


## -description


Retrieves the user's warning threshold for the volume. This threshold is expressed as a text string, for example "10.5 MB". If the user's threshold is unlimited, the string returned is "No Limit" (localized). If the destination buffer is too small, the string is truncated to fit the buffer.


## -parameters




### -param pszText [out]

The text string.
					


### -param cchText [in]

The size of the destination buffer, in characters.


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
 

 

