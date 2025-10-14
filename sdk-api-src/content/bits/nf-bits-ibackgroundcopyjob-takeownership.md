---
UID: NF:bits.IBackgroundCopyJob.TakeOwnership
title: IBackgroundCopyJob::TakeOwnership (bits.h)
description: Changes ownership of the job to the current user.
helpviewer_keywords: ["IBackgroundCopyJob interface [BITS]","TakeOwnership method","IBackgroundCopyJob.TakeOwnership","IBackgroundCopyJob::TakeOwnership","TakeOwnership","TakeOwnership method [BITS]","TakeOwnership method [BITS]","IBackgroundCopyJob interface","_drz_ibackgroundcopyjob_takeownership","bits.ibackgroundcopyjob_takeownership","bits/IBackgroundCopyJob::TakeOwnership"]
old-location: bits\ibackgroundcopyjob_takeownership.htm
tech.root: Bits
ms.assetid: 12ac2dd8-516b-4b5d-a2bf-0abb55d18ee0
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJob interface [BITS],TakeOwnership method, IBackgroundCopyJob.TakeOwnership, IBackgroundCopyJob::TakeOwnership, TakeOwnership, TakeOwnership method [BITS], TakeOwnership method [BITS],IBackgroundCopyJob interface, _drz_ibackgroundcopyjob_takeownership, bits.ibackgroundcopyjob_takeownership, bits/IBackgroundCopyJob::TakeOwnership
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
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJob::TakeOwnership
 - bits/IBackgroundCopyJob::TakeOwnership
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyJob.TakeOwnership
---

# IBackgroundCopyJob::TakeOwnership


## -description

Changes ownership of the job to the current user.



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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Job ownership was successfully changed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_NEW_OWNER_NO_FILE_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
The new owner has insufficient access to the temporary files on the client computer. BITS creates the temporary files using the owner's security permissions.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_NEW_OWNER_DIFF_MAPPING</b></dt>
</dl>
</td>
<td width="60%">
The current owner's network drive mapping for the local file is different from the previous owner's.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
User does not have administrator privileges.

</td>
</tr>
</table>

## -remarks

To take ownership of the job, the user must have administrator privileges on the client. On Windows Vista, the user must run in an elevated state. After taking ownership, any future updates to the job must be done while the user is running in an elevated state. For details, see <a href="/windows/desktop/Bits/users-and-network-connections">Users and Network Connections</a>.

An administrator does not have to take ownership of another user's job to change its properties or to add files to the job. Typically, an administrator uses the 
<b>TakeOwnership</b> method if the user does not have sufficient permission to complete the job or if the user is not logged on and the administrator needs the job to complete.

After ownership of the job has changed, the job is processed only when the new owner is logged on to the client. Call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getowner">IBackgroundCopyJob::GetOwner</a> method to retrieve the SID of the new owner.

If the administrator 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-cancel">cancels</a> the job after taking ownership, it is possible that the files may be orphaned because the administrator does not have write permission to the files. This can occur if the local file destination is in the previous user's roaming profile.

The 
<b>TakeOwnership</b> method removes 
<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials">credentials</a>, <a href="/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyid">certificates</a>, <a href="/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setcustomheaders">custom headers</a>, and 
<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline">command line notification</a> from the job, if set.

If the job specifies <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyinterface">event notification</a>, the callback is executed in the context of the user who called the <b>IBackgroundCopyJob::SetNotifyInterface</b> method.

## -see-also

<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getowner">IBackgroundCopyJob::GetOwner</a>
