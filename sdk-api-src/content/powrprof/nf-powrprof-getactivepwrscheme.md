---
UID: NF:powrprof.GetActivePwrScheme
title: GetActivePwrScheme function (powrprof.h)
description: Retrieves the index of the active power scheme.
helpviewer_keywords: ["GetActivePwrScheme","GetActivePwrScheme function","_win32_getactivepwrscheme","base.getactivepwrscheme","powrprof/GetActivePwrScheme"]
old-location: base\getactivepwrscheme.htm
tech.root: base
ms.assetid: 2a321372-40ff-4292-8b66-db3f794e5f53
ms.date: 12/05/2018
ms.keywords: GetActivePwrScheme, GetActivePwrScheme function, _win32_getactivepwrscheme, base.getactivepwrscheme, powrprof/GetActivePwrScheme
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
 - GetActivePwrScheme
 - powrprof/GetActivePwrScheme
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
 - GetActivePwrScheme
---

# GetActivePwrScheme function


## -description

<p class="CCE_Message">[<b>GetActivePwrScheme</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Applications written for Windows Vista and later should use <a href="/windows/desktop/api/powersetting/nf-powersetting-powergetactivescheme">PowerGetActiveScheme</a> instead.]

Retrieves the index of the active power scheme.

## -parameters

### -param puiID [out]

A pointer to a variable that receives the index of the active power scheme.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The active power scheme remains active until either the user sets a new power scheme using the Power Options control panel program, or an application calls the 
<a href="/windows/desktop/api/powrprof/nf-powrprof-setactivepwrscheme">SetActivePwrScheme</a> function.

For more information on using PowrProf.h, see <a href="/windows/desktop/Power/power-schemes">Power Schemes</a>.

## -see-also

<a href="/windows/desktop/Power/power-management-functions">Power Management Functions</a>



<a href="/windows/desktop/Power/power-schemes">Power Schemes</a>



<a href="/windows/desktop/api/powrprof/nf-powrprof-setactivepwrscheme">SetActivePwrScheme</a>