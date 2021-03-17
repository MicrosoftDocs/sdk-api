---
UID: NF:clfsmgmtw32.SetLogFileSizeWithPolicy
title: SetLogFileSizeWithPolicy function (clfsmgmtw32.h)
description: Adds or deletes containers from a log based on the state of the installed policies.
helpviewer_keywords: ["SetLogFileSizeWithPolicy","SetLogFileSizeWithPolicy function [Files]","clfsmgmtw32/SetLogFileSizeWithPolicy","fs.setlogfilesizewithpolicy"]
old-location: fs\setlogfilesizewithpolicy.htm
tech.root: fs
ms.assetid: 4da401cf-3606-4ae1-ae6f-37eb3dea6426
ms.date: 12/05/2018
ms.keywords: SetLogFileSizeWithPolicy, SetLogFileSizeWithPolicy function [Files], clfsmgmtw32/SetLogFileSizeWithPolicy, fs.setlogfilesizewithpolicy
req.header: clfsmgmtw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetLogFileSizeWithPolicy
 - clfsmgmtw32/SetLogFileSizeWithPolicy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - SetLogFileSizeWithPolicy
---

# SetLogFileSizeWithPolicy function


## -description

Adds or deletes containers from a log based on the state of the installed policies.

## -parameters

### -param hLog [in]

A handle to a log.

### -param pDesiredSize [in]

A pointer to a value that specifies the requested log size, expressed as one of the following values. For the actual resultant size, refer to the <i>pResultingSize</i> parameter.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Enforce the minimum size policy.

If a minimum size policy is not installed, one of the following occurs:
<ul>
<li>If the log has fewer than two containers, the log will be expanded to a size of two containers.</li>
<li>If the log has two or more containers, no changes are made and the function call succeeds.</li>
</ul>


If a minimum size policy is installed, one of the following occurs:<ul>
<li>If the log has fewer than the minimum number of containers specified by the minimum size policy, the log expands to the policy-specified minimum number of containers.</li>
<li>If the log has a number of containers greater than or equal to the minimum number of containers specified by the minimum size policy,  no changes are made and the function call succeeds with no error.</li>
</ul>


For more information, see <a href="/windows/desktop/api/clfsmgmtw32/nf-clfsmgmtw32-installlogpolicy">InstallLogPolicy</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Not a valid value; the function call fails with <b>ERROR_INVALID_PARAMETER</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2–1023</dt>
</dl>
</td>
<td width="60%">
The desired size of the log, expressed as the number of containers. 

If this number is smaller than the minimum number of containers specified by the installed policy, the function call fails with <b>ERROR_COULD_NOT_RESIZE_LOG</b>.

If this number is larger than the maximum number of containers specified by the installed policy, the log expands only as far as the policy-specified maximum number of containers, and the function succeeds with no error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1024–MAXULONGLONG</dt>
</dl>
</td>
<td width="60%">
If no maximum size policy is installed, the function call fails with <b>ERROR_LOG_POLICY_CONFLICT</b>.

If a maximum size policy is installed, the log expands to the maximum number of containers specified by the maximum size policy and the function succeeds with no error.

</td>
</tr>
</table>

### -param pResultingSize [out]

A pointer to a valid ULONGLONG data variable, receives the number of containers in the resized log upon success.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

Containers are  created using the same security attributes as   the .blf file and are created within the context of the application, not the context of the owner of the .blf file. For more information about .blf files, see <a href="/previous-versions/windows/desktop/clfs/log-types">Log Types</a>. If containers are deleted, they are deleted using the security context of the calling application.


#### Examples

For an example that uses this function, see <a href="/previous-versions/windows/desktop/clfs/creating-a-log-file">Creating a Log File</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/clfs/creating-a-log-file">Creating a Log File</a>



<a href="/windows/desktop/api/clfsmgmtw32/nf-clfsmgmtw32-installlogpolicy">InstallLogPolicy</a>



<a href="/previous-versions/windows/desktop/clfs/log-types">Log Types</a>