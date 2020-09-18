---
UID: NF:winbase.RegisterApplicationRecoveryCallback
title: RegisterApplicationRecoveryCallback function (winbase.h)
description: Registers the active instance of an application for recovery.
helpviewer_keywords: ["RegisterApplicationRecoveryCallback","RegisterApplicationRecoveryCallback function [Recovery]","base.registerapplicationrecoverycallback","recovery.registerapplicationrecoverycallback","winbase/RegisterApplicationRecoveryCallback"]
old-location: recovery\registerapplicationrecoverycallback.htm
tech.root: Recovery
ms.assetid: 4ff73c2c-a941-4626-ae40-cafbe6e50644
ms.date: 12/05/2018
ms.keywords: RegisterApplicationRecoveryCallback, RegisterApplicationRecoveryCallback function [Recovery], base.registerapplicationrecoverycallback, recovery.registerapplicationrecoverycallback, winbase/RegisterApplicationRecoveryCallback
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegisterApplicationRecoveryCallback
 - winbase/RegisterApplicationRecoveryCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - RegisterApplicationRecoveryCallback
---

# RegisterApplicationRecoveryCallback function


## -description

Registers the active instance of an application for recovery.

## -parameters

### -param pRecoveyCallback [in]

A pointer to the recovery callback function. For more information, see <a href="/previous-versions/windows/desktop/legacy/aa373202(v=vs.85)">ApplicationRecoveryCallback</a>.

### -param pvParameter [in, optional]

A pointer to a variable to be passed to the callback function. Can be <b>NULL</b>.

### -param dwPingInterval [in]

The recovery ping interval, in milliseconds. By default, the interval is 5 seconds (RECOVERY_DEFAULT_PING_INTERVAL). The maximum interval is 5 minutes. If you specify zero, the default interval is used. 

You must call the <a href="/windows/desktop/api/winbase/nf-winbase-applicationrecoveryinprogress">ApplicationRecoveryInProgress</a> function within the specified interval to indicate to ARR that you are still actively recovering; otherwise, WER terminates recovery. Typically, you perform recovery in a loop with each iteration lasting no longer than the ping interval. Each iteration performs a block of recovery work followed by a call to <b>ApplicationRecoveryInProgress</b>. Since you also use <b>ApplicationRecoveryInProgress</b> to determine if the user wants to cancel recovery, you should consider a smaller interval, so you do not perform a lot of work unnecessarily.

### -param dwFlags [in]

Reserved for future use. Set to zero.

## -returns

This function returns <b>S_OK</b> on success or one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Internal error; the registration failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The ping interval cannot be more than five minutes.

</td>
</tr>
</table>

## -remarks

If the  application encounters an unhandled exception or becomes unresponsive, Windows Error Reporting (WER) calls the specified recovery callback. You should use the callback to save data and state information. You can use the information if you also call  the <a href="/windows/desktop/api/winbase/nf-winbase-registerapplicationrestart">RegisterApplicationRestart</a> function to request that WER restart the application.

WER will not call your recovery callback if an installer wants to  update a component of your application. To save data and state information in the update case, you should handle the <a href="/windows/desktop/Shutdown/wm-queryendsession">WM_QUERYENDSESSION</a> and <a href="/windows/desktop/Shutdown/wm-endsession">WM_ENDSESSION</a> messages. For details, see each message. The timeout for responding to these messages is five seconds. Most of the available recovery time is in the <a href="/windows/desktop/winmsg/wm-close">WM_CLOSE</a> message for which you have 30 seconds.

A console application that can be updated uses the CTRL_C_EVENT notification to initiate recovery (for details, see the <a href="/windows/console/handlerroutine">HandlerRoutine</a> callback function). The timeout for the handler to complete is 30 seconds.

Applications should consider saving data and state information on a periodic bases to shorten the amount of time required for recovery.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa373202(v=vs.85)">ApplicationRecoveryCallback</a>



<a href="/windows/desktop/api/winbase/nf-winbase-applicationrecoveryinprogress">ApplicationRecoveryInProgress</a>



<a href="/windows/desktop/api/winbase/nf-winbase-registerapplicationrestart">RegisterApplicationRestart</a>



<a href="/windows/desktop/api/winbase/nf-winbase-unregisterapplicationrecoverycallback">UnregisterApplicationRecoveryCallback</a>