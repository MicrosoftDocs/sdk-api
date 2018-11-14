---
UID: NF:dskquota.IDiskQuotaControl.SetDefaultQuotaLimit
title: IDiskQuotaControl::SetDefaultQuotaLimit
author: windows-sdk-content
description: Modifies the default quota limit.
old-location: fs\idiskquotacontrol_setdefaultquotalimit.htm
tech.root: fileio
ms.assetid: 2e4d8d04-dff2-477f-a5b2-8c8415cb3b52
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IDiskQuotaControl interface [Files],SetDefaultQuotaLimit method, IDiskQuotaControl.SetDefaultQuotaLimit, IDiskQuotaControl::SetDefaultQuotaLimit, SetDefaultQuotaLimit, SetDefaultQuotaLimit method [Files], SetDefaultQuotaLimit method [Files],IDiskQuotaControl interface, _win32_idiskquotacontrol_setdefaultquotalimit, base.idiskquotacontrol_setdefaultquotalimit, dskquota/IDiskQuotaControl::SetDefaultQuotaLimit, fs.idiskquotacontrol_setdefaultquotalimit
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
 - IDiskQuotaControl.SetDefaultQuotaLimit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dskquota.h
: 
- IDiskQuotaControl.SetDefaultQuotaLimit
: 
---

# IDiskQuotaControl::SetDefaultQuotaLimit


## -description


Modifies the default quota limit. This limit is applied automatically to new users of the volume.


## -parameters




### -param llLimit [in]

The default quota limit, in bytes. If this value is -1, the user has an unlimited quota.


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
<dt><b>ERROR_NOT_READY</b></dt>
</dl>
</td>
<td width="60%">
The <b>DiskQuotaControl</b> object is not initialized.

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



<a href="https://msdn.microsoft.com/fc9add5a-c9ef-462d-8125-128d48018717">IDiskQuotaControl</a>
 

 

