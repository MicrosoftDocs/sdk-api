---
UID: NF:atacct.SetNetScheduleAccountInformation
title: SetNetScheduleAccountInformation function (atacct.h)
description: The SetNetScheduleAccountInformation function sets the AT Service account name and password. The AT Service account name and password are used as the credentials for scheduled jobs created with NetScheduleJobAdd.
helpviewer_keywords: ["SetNetScheduleAccountInformation","SetNetScheduleAccountInformation function [Network Management]","atacct/SetNetScheduleAccountInformation","netmgmt.setnetscheduleaccountinformation"]
old-location: netmgmt\setnetscheduleaccountinformation.htm
tech.root: NetMgmt
ms.assetid: e45cc3d6-f0dd-4c24-967e-4db08078d15e
ms.date: 12/05/2018
ms.keywords: SetNetScheduleAccountInformation, SetNetScheduleAccountInformation function [Network Management], atacct/SetNetScheduleAccountInformation, netmgmt.setnetscheduleaccountinformation
req.header: atacct.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP1 [desktop apps only]
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
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetNetScheduleAccountInformation
 - atacct/SetNetScheduleAccountInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mstask.dll
api_name:
 - SetNetScheduleAccountInformation
---

# SetNetScheduleAccountInformation function


## -description

<p class="CCE_Message">[<b>SetNetScheduleAccountInformation</b> is no longer available for use as of Windows 8. Instead, use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces"> Task Scheduler 2.0 Interfaces</a>.

]

The <b>SetNetScheduleAccountInformation</b> function sets the AT Service account name and password. The AT Service account name and password are used as the credentials for scheduled jobs created with <a href="/windows/desktop/api/lmat/nf-lmat-netschedulejobadd">NetScheduleJobAdd</a>.

## -parameters

### -param pwszServerName [in]

A NULL-terminated wide character string for the name of the computer whose account information is being set.

### -param pwszAccount [in]

A pointer to a NULL-terminated wide character string for the account. To specify the local system account, set this parameter to <b>NULL</b>.

### -param pwszPassword [in]

A pointer to a NULL-terminated wide character string for the password. For information about securing password information, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.

## -returns

The return value is an HRESULT. A value of S_OK indicates the account name and password were successfully set. Any other value indicates an error condition.

If the function fails, some of the possible return values are listed below. 

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
<dt>0x080070005</dt>
</dl>
</td>
<td width="60%">
Access was denied. This error is returned if the caller was not a member of the Administrators group. This error is also returned if the <i>pwszAccount</i> parameter  was  not <b>NULL</b> indicating a named account not the local system account and the <i>pwszPassword</i> parameter was incorrect for the account specified in the <i>pwszAccount</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_DATA)</b></dt>
<dt>0x08007000d</dt>
</dl>
</td>
<td width="60%">
The data is invalid. This error is returned if the <i>pwszPassword</i> parameter was <b>NULL</b> or the length of  <i>pwszPassword</i> parameter string was too long.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCHED_E_ACCOUNT_NAME_NOT_FOUND</b></dt>
<dt>0x80041310</dt>
</dl>
</td>
<td width="60%">
Unable to establish existence of the account specified. This error is returned if the <i>pwszAccount</i> parameter  was  not <b>NULL</b> indicating a named account not the local system account and  the <i>pwszAccount</i> parameter could not be found. 

</td>
</tr>
</table>

## -remarks

The <b>SetNetScheduleAccountInformation</b> impersonates the caller. Only members of the local Administrators group on the computer where the schedule account information is being set can successfully execute this function. Note that <b>NULL</b> passwords are not allowed.

## -see-also

<a href="/windows/desktop/api/atacct/nf-atacct-getnetscheduleaccountinformation">GetNetScheduleAccountInformation</a>