---
UID: NC:userenv.PFNSTATUSMESSAGECALLBACK
title: PFNSTATUSMESSAGECALLBACK (userenv.h)
description: The StatusMessageCallback function is an application-defined callback function used to display status messages when applying policy.
helpviewer_keywords: ["PFNSTATUSMESSAGECALLBACK","PFNSTATUSMESSAGECALLBACK callback","PFNSTATUSMESSAGECALLBACK callback function [Group Policy]","StatusMessageCallback","_win32_statusmessagecallback","policy.statusmessagecallback","userenv/PFNSTATUSMESSAGECALLBACK"]
old-location: policy\statusmessagecallback.htm
tech.root: Policy
ms.assetid: 9eec6204-49b5-49fd-8db4-5c1777eb7c85
ms.date: 12/05/2018
ms.keywords: PFNSTATUSMESSAGECALLBACK, PFNSTATUSMESSAGECALLBACK callback, PFNSTATUSMESSAGECALLBACK callback function [Group Policy], StatusMessageCallback, _win32_statusmessagecallback, policy.statusmessagecallback, userenv/PFNSTATUSMESSAGECALLBACK
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFNSTATUSMESSAGECALLBACK
 - userenv/PFNSTATUSMESSAGECALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Userenv.h
api_name:
 - PFNSTATUSMESSAGECALLBACK
---

# PFNSTATUSMESSAGECALLBACK callback function


## -description

The
    <b>StatusMessageCallback</b> function is an application-defined callback function used to display status messages when applying policy. The <b>PFNSTATUSMESSAGECALLBACK</b> type defines a pointer to this callback function. 
<b>StatusMessageCallback</b> is a placeholder for the application-defined function name.

## -parameters

### -param bVerbose [in]

Specifies whether the message is verbose. If this parameter is <b>TRUE</b>, the message is verbose. If this parameter is <b>FALSE</b>, the message is not verbose.

### -param lpMessage [in]

Pointer to a buffer that contains the message string.

## -returns

If the message was displayed successfully, return <b>ERROR_SUCCESS</b>. Otherwise, return a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

Pass a pointer to the 
<b>StatusMessageCallback</b> function when the system calls the 
<a href="/windows/desktop/api/userenv/nc-userenv-pfnprocessgrouppolicy">ProcessGroupPolicy</a> or the 
<a href="/windows/desktop/api/userenv/nc-userenv-pfnprocessgrouppolicyex">ProcessGroupPolicyEx</a> callback function.

The status user interface has two modes: standard and verbose. Verbose messages are displayed only when the computer is in verbose mode. To enable verbose mode, set the following registry value to 1, log out, and log on. There is no need to restart the computer.


<b>HKEY_LOCAL_MACHINE</b>&#92;<b>Software</b>&#92;<b>Microsoft</b>&#92;<b>Windows NT</b>&#92;<b>CurrentVersion</b>&#92;<b>Winlogon</b>&#92;<b>VerboseStatus</b>



<div class="alert"><b>Warning</b>  Do not call the 
<b>StatusMessageCallback</b> function from a background thread because you may overwrite another thread's status message.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/windows/desktop/api/userenv/nc-userenv-pfnprocessgrouppolicy">ProcessGroupPolicy</a>



<a href="/windows/desktop/api/userenv/nc-userenv-pfnprocessgrouppolicyex">ProcessGroupPolicyEx</a>