---
UID: NF:dskquota.IDiskQuotaControl.GetQuotaState
title: IDiskQuotaControl::GetQuotaState
author: windows-sdk-content
description: Retrieves a set of flags describing the state of the quota system.
old-location: fs\idiskquotacontrol_getquotastate.htm
tech.root: FileIO
ms.assetid: 1e35be3e-095a-4299-933d-6ebf3ccc5a1c
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: DISKQUOTA_FILESTATE_INCOMPLETE, DISKQUOTA_FILESTATE_REBUILDING, DISKQUOTA_STATE_DISABLED, DISKQUOTA_STATE_ENFORCE, DISKQUOTA_STATE_TRACK, GetQuotaState, GetQuotaState method [Files], GetQuotaState method [Files],IDiskQuotaControl interface, IDiskQuotaControl interface [Files],GetQuotaState method, IDiskQuotaControl.GetQuotaState, IDiskQuotaControl::GetQuotaState, _win32_idiskquotacontrol_getquotastate, base.idiskquotacontrol_getquotastate, dskquota/IDiskQuotaControl::GetQuotaState, fs.idiskquotacontrol_getquotastate
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
 - IDiskQuotaControl.GetQuotaState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiskQuotaControl::GetQuotaState


## -description


Retrieves a set of flags describing the state of the quota system.


## -parameters




### -param pdwState [out]

The quota state flags. This parameter can include one or more of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DISKQUOTA_FILESTATE_INCOMPLETE"></a><a id="diskquota_filestate_incomplete"></a><dl>
<dt><b>DISKQUOTA_FILESTATE_INCOMPLETE</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
The volume's quota information is out of date. Quotas are probably disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="DISKQUOTA_FILESTATE_REBUILDING"></a><a id="diskquota_filestate_rebuilding"></a><dl>
<dt><b>DISKQUOTA_FILESTATE_REBUILDING</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
The volume is rebuilding its quota information.

</td>
</tr>
<tr>
<td width="40%"><a id="DISKQUOTA_STATE_DISABLED"></a><a id="diskquota_state_disabled"></a><dl>
<dt><b>DISKQUOTA_STATE_DISABLED</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Quotas are not enabled on the volume.

</td>
</tr>
<tr>
<td width="40%"><a id="DISKQUOTA_STATE_ENFORCE"></a><a id="diskquota_state_enforce"></a><dl>
<dt><b>DISKQUOTA_STATE_ENFORCE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Quotas are enabled and the limit value is enforced. Users cannot exceed their quota limit.

</td>
</tr>
<tr>
<td width="40%"><a id="DISKQUOTA_STATE_TRACK"></a><a id="diskquota_state_track"></a><dl>
<dt><b>DISKQUOTA_STATE_TRACK</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Quotas are enabled but the limit value is not being enforced. Users may exceed their quota limit.

</td>
</tr>
</table>
 


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pdwState</i> parameter is incorrect.

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
 

 

