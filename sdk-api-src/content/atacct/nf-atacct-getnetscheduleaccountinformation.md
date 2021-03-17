---
UID: NF:atacct.GetNetScheduleAccountInformation
title: GetNetScheduleAccountInformation function (atacct.h)
description: The GetNetScheduleAccountInformation function retrieves the AT Service account name.
helpviewer_keywords: ["GetNetScheduleAccountInformation","GetNetScheduleAccountInformation function [Network Management]","atacct/GetNetScheduleAccountInformation","netmgmt.getnetscheduleaccountinformation"]
old-location: netmgmt\getnetscheduleaccountinformation.htm
tech.root: NetMgmt
ms.assetid: 935de94a-6791-4ea2-ac39-cf71ef7cb726
ms.date: 12/05/2018
ms.keywords: GetNetScheduleAccountInformation, GetNetScheduleAccountInformation function [Network Management], atacct/GetNetScheduleAccountInformation, netmgmt.getnetscheduleaccountinformation
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
 - GetNetScheduleAccountInformation
 - atacct/GetNetScheduleAccountInformation
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
 - GetNetScheduleAccountInformation
---

# GetNetScheduleAccountInformation function


## -description

<p class="CCE_Message">[<b>GetNetScheduleAccountInformation</b> is no longer available for use as of Windows 8. Instead, use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces"> Task Scheduler 2.0 Interfaces</a>.

]

The <b>GetNetScheduleAccountInformation</b> function retrieves the AT Service account name.

## -parameters

### -param pwszServerName [in]

A NULL-terminated wide character string for the name of the computer whose account information is being retrieved.

### -param ccAccount [in]

The number of characters, including the NULL terminator, allocated for <i>wszAccount</i>. The maximum allowed length for this value is the maximum domain name length plus the maximum user name length plus 2, expressed as DNLEN + UNLEN + 2. (The last two characters are the "\" character and the NULL terminator.)

### -param wszAccount [out]

An array of wide characters, including the NULL terminator, that receives the account information.

## -returns

The return value is an HRESULT. A value of S_OK indicates the function succeeded, and the account information is  returned in <i>wszAccount</i>. A value of S_FALSE  indicates the function succeeded, and the account is the Local System account (no information will be returned in <i>wszAccount</i>). Any other return values indicate an error condition.

## -remarks

To successfully call the <b>GetNetScheduleAccountInformation</b> function,  the caller should have read access to the task folder  which is usually %windir%\tasks or as defined in the following registry setting:

<b>HKLM\SOFTWARE\Microsoft\SchedulingAgent\TasksFolder\
</b>

## -see-also

<a href="/windows/desktop/api/atacct/nf-atacct-setnetscheduleaccountinformation">SetNetScheduleAccountInformation</a>