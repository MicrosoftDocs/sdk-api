---
UID: NF:dskquota.IDiskQuotaUser.GetQuotaLimit
title: IDiskQuotaUser::GetQuotaLimit (dskquota.h)
description: Retrieves the user's quota limit value on the volume.
helpviewer_keywords: ["GetQuotaLimit","GetQuotaLimit method [Files]","GetQuotaLimit method [Files]","IDiskQuotaUser interface","IDiskQuotaUser interface [Files]","GetQuotaLimit method","IDiskQuotaUser.GetQuotaLimit","IDiskQuotaUser::GetQuotaLimit","_win32_idiskquotauser_getquotalimit","base.idiskquotauser_getquotalimit","dskquota/IDiskQuotaUser::GetQuotaLimit","fs.idiskquotauser_getquotalimit"]
old-location: fs\idiskquotauser_getquotalimit.htm
tech.root: fs
ms.assetid: 77b9099c-7696-47d8-ac08-b58a329909ee
ms.date: 12/05/2018
ms.keywords: GetQuotaLimit, GetQuotaLimit method [Files], GetQuotaLimit method [Files],IDiskQuotaUser interface, IDiskQuotaUser interface [Files],GetQuotaLimit method, IDiskQuotaUser.GetQuotaLimit, IDiskQuotaUser::GetQuotaLimit, _win32_idiskquotauser_getquotalimit, base.idiskquotauser_getquotalimit, dskquota/IDiskQuotaUser::GetQuotaLimit, fs.idiskquotauser_getquotalimit
f1_keywords:
- dskquota/IDiskQuotaUser.GetQuotaLimit
dev_langs:
- c++
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
- IDiskQuotaUser.GetQuotaLimit
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDiskQuotaUser::GetQuotaLimit


## -description


Retrieves the user's quota limit value on the volume. The limit is set as the maximum amount of disk space available to the volume user.


## -parameters




### -param pllLimit [out]

The limit value. If this value is –1, the user has an unlimited quota.


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
The <i>pllLimit</i> parameter is <b>NULL</b>.

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




<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nn-dskquota-idiskquotauser">IDiskQuotaUser</a>
 

 

