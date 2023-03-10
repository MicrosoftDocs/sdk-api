---
UID: NF:dskquota.IDiskQuotaControl.GiveUserNameResolutionPriority
title: IDiskQuotaControl::GiveUserNameResolutionPriority (dskquota.h)
description: Promotes the specified user object to the head of the queue so that it is next in line for resolution.
helpviewer_keywords: ["GiveUserNameResolutionPriority","GiveUserNameResolutionPriority method [Files]","GiveUserNameResolutionPriority method [Files]","IDiskQuotaControl interface","IDiskQuotaControl interface [Files]","GiveUserNameResolutionPriority method","IDiskQuotaControl.GiveUserNameResolutionPriority","IDiskQuotaControl::GiveUserNameResolutionPriority","_win32_idiskquotacontrol_giveusernameresolutionpriority","base.idiskquotacontrol_giveusernameresolutionpriority","dskquota/IDiskQuotaControl::GiveUserNameResolutionPriority","fs.idiskquotacontrol_giveusernameresolutionpriority"]
old-location: fs\idiskquotacontrol_giveusernameresolutionpriority.htm
tech.root: fs
ms.assetid: 07de4fc4-e68f-405d-bb96-14ccad37e8e8
ms.date: 12/05/2018
ms.keywords: GiveUserNameResolutionPriority, GiveUserNameResolutionPriority method [Files], GiveUserNameResolutionPriority method [Files],IDiskQuotaControl interface, IDiskQuotaControl interface [Files],GiveUserNameResolutionPriority method, IDiskQuotaControl.GiveUserNameResolutionPriority, IDiskQuotaControl::GiveUserNameResolutionPriority, _win32_idiskquotacontrol_giveusernameresolutionpriority, base.idiskquotacontrol_giveusernameresolutionpriority, dskquota/IDiskQuotaControl::GiveUserNameResolutionPriority, fs.idiskquotacontrol_giveusernameresolutionpriority
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDiskQuotaControl::GiveUserNameResolutionPriority
 - dskquota/IDiskQuotaControl::GiveUserNameResolutionPriority
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dskquota.dll
api_name:
 - IDiskQuotaControl.GiveUserNameResolutionPriority
---

# IDiskQuotaControl::GiveUserNameResolutionPriority


## -description

Promotes the specified user object to the head of the queue so that it is next in line for resolution. By default, quota user objects are serviced in the order in which they were placed in the queue.

This method is applicable only when asynchronous name resolution is used.

## -parameters

### -param pUser [in]

A pointer to the 
<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotauser">IDiskQuotaUser</a> interface.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Quota user object not in the resolver queue.

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

<a href="/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>



<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotacontrol">IDiskQuotaControl</a>