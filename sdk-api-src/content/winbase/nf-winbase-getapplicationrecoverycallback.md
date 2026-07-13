---
UID: NF:winbase.GetApplicationRecoveryCallback
title: GetApplicationRecoveryCallback function (winbase.h)
description: Retrieves a pointer to the callback routine registered for the specified process. The address returned is in the virtual address space of the process.
helpviewer_keywords: ["GetApplicationRecoveryCallback","GetApplicationRecoveryCallback function [Recovery]","base.getapplicationrecoverycallback","recovery.getapplicationrecoverycallback","winbase/GetApplicationRecoveryCallback"]
old-location: recovery\getapplicationrecoverycallback.htm
tech.root: Recovery
ms.assetid: 974147de-1249-4062-a492-4db9646043c6
ms.date: 12/05/2018
ms.keywords: GetApplicationRecoveryCallback, GetApplicationRecoveryCallback function [Recovery], base.getapplicationrecoverycallback, recovery.getapplicationrecoverycallback, winbase/GetApplicationRecoveryCallback
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
 - GetApplicationRecoveryCallback
 - winbase/GetApplicationRecoveryCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-windowserrorreporting-l1-1-3.dll
 - api-ms-win-core-windowserrorreporting-l1-1-2.dll
 - api-ms-win-core-windowserrorreporting-l1-1-1.dll
 - Kernel32.dll
 - API-MS-Win-Core-Windowserrorreporting-l1-1-0.dll
 - KernelBase.dll
api_name:
 - GetApplicationRecoveryCallback
---

# GetApplicationRecoveryCallback function


## -description

Retrieves  a pointer to the callback routine registered for the specified process. The address returned is in the virtual address space of the process.

## -parameters

### -param hProcess [in]

A handle to the process. This handle must have the PROCESS_VM_READ access right.

### -param pRecoveryCallback [out]

A pointer to the recovery callback function. For more information, see <a href="/previous-versions/windows/desktop/legacy/aa373202(v=vs.85)">ApplicationRecoveryCallback</a>.

### -param ppvParameter [out]

A pointer to the callback parameter.

### -param pdwPingInterval [out]

The recovery ping interval, in 100-nanosecond intervals.

### -param pdwFlags [out]

Reserved for future use.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The application did not register for recovery.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-registerapplicationrecoverycallback">RegisterApplicationRecoveryCallback</a>