---
UID: NF:powrprof.DeletePwrScheme
title: DeletePwrScheme function (powrprof.h)
description: Deletes the specified power scheme.
helpviewer_keywords: ["DeletePwrScheme","DeletePwrScheme function","_win32_deletepwrscheme","base.deletepwrscheme","powrprof/DeletePwrScheme"]
old-location: base\deletepwrscheme.htm
tech.root: base
ms.assetid: c9513835-00c4-4260-a8b6-d947539c9dd1
ms.date: 12/05/2018
ms.keywords: DeletePwrScheme, DeletePwrScheme function, _win32_deletepwrscheme, base.deletepwrscheme, powrprof/DeletePwrScheme
req.header: powrprof.h
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
req.lib: PowrProf.lib
req.dll: PowrProf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DeletePwrScheme
 - powrprof/DeletePwrScheme
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PowrProf.dll
api_name:
 - DeletePwrScheme
---

# DeletePwrScheme function


## -description

<p class="CCE_Message">[<b>DeletePwrScheme</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Applications written for Windows Vista and later should use <a href="/windows/desktop/api/powrprof/nf-powrprof-powerdeletescheme">PowerDeleteScheme</a> instead.]

Deletes the specified power scheme.

## -parameters

### -param uiID [in]

The index of the power scheme to be deleted.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Applications can call 
<b>DeletePwrScheme</b> to permanently delete a power scheme. An attempt to delete the currently active power scheme fails with the last error set to ERROR_ACCESS_DENIED.

For more information on using PowrProf.h, see <a href="/windows/desktop/Power/power-schemes">Power Schemes</a>.

## -see-also

<a href="/windows/desktop/Power/power-management-functions">Power Management Functions</a>



<a href="/windows/desktop/Power/power-schemes">Power Schemes</a>



<a href="/windows/desktop/api/powrprof/nf-powrprof-writepwrscheme">WritePwrScheme</a>