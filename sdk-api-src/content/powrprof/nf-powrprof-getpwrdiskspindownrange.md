---
UID: NF:powrprof.GetPwrDiskSpindownRange
title: GetPwrDiskSpindownRange function (powrprof.h)
description: Retrieves the disk spindown range.
helpviewer_keywords: ["GetPwrDiskSpindownRange","GetPwrDiskSpindownRange function","_win32_getpwrdiskspindownrange","base.getpwrdiskspindownrange","powrprof/GetPwrDiskSpindownRange"]
old-location: base\getpwrdiskspindownrange.htm
tech.root: base
ms.assetid: c56f679d-512a-4bf9-89dc-8905bba8c6ce
ms.date: 12/05/2018
ms.keywords: GetPwrDiskSpindownRange, GetPwrDiskSpindownRange function, _win32_getpwrdiskspindownrange, base.getpwrdiskspindownrange, powrprof/GetPwrDiskSpindownRange
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
 - GetPwrDiskSpindownRange
 - powrprof/GetPwrDiskSpindownRange
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
 - GetPwrDiskSpindownRange
---

# GetPwrDiskSpindownRange function


## -description

<p class="CCE_Message">[<b>GetPwrDiskSpindownRange</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. See Remarks.]

Retrieves the disk spindown range.

## -parameters

### -param puiMax [out]

The maximum disk spindown time, in seconds.

### -param puiMin [out]

The minimum disk spindown time, in seconds.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Starting with Windows Vista, power management configuration of the system's hard disk drives is controlled through the GUID_DISK_SUBGROUP power settings subgroup. Use the <a href="/windows/desktop/api/powrprof/nf-powrprof-powerenumerate">PowerEnumerate</a> function to enumerate individual settings.

For more information on using PowrProf.h, see <a href="/windows/desktop/Power/power-schemes">Power Schemes</a>.

## -see-also

<a href="/windows/desktop/api/powerbase/nf-powerbase-callntpowerinformation">CallNtPowerInformation</a>



<a href="/windows/desktop/Power/power-management-functions">Power Management Functions</a>