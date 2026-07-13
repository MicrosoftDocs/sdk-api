---
UID: NF:winbase.GetDefaultCommConfigA
title: GetDefaultCommConfigA function (winbase.h)
description: Retrieves the default configuration for the specified communications device. (ANSI)
helpviewer_keywords: ["GetDefaultCommConfigA", "winbase/GetDefaultCommConfigA"]
old-location: base\getdefaultcommconfig.htm
tech.root: base
ms.assetid: 04bf5033-17c3-4403-8386-f3144e11423f
ms.date: 12/05/2018
ms.keywords: GetDefaultCommConfig, GetDefaultCommConfig function, GetDefaultCommConfigA, GetDefaultCommConfigW, _win32_getdefaultcommconfig, base.getdefaultcommconfig, winbase/GetDefaultCommConfig, winbase/GetDefaultCommConfigA, winbase/GetDefaultCommConfigW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetDefaultCommConfigW (Unicode) and GetDefaultCommConfigA (ANSI)
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
 - GetDefaultCommConfigA
 - winbase/GetDefaultCommConfigA
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
 - GetDefaultCommConfig
 - GetDefaultCommConfigA
 - GetDefaultCommConfigW
---

# GetDefaultCommConfigA function


## -description

Retrieves the default configuration for the specified communications device.

## -parameters

### -param lpszName [in]

The name of the device. For example, COM1 through COM9 are serial ports and LPT1 through LPT9 are parallel ports.

### -param lpCC [out]

A pointer to a buffer that receives a 
<a href="/windows/desktop/api/winbase/ns-winbase-commconfig">COMMCONFIG</a> structure.

### -param lpdwSize [in, out]

A pointer to a variable that specifies the size of the buffer pointed to by <i>lpCC</i>, in bytes. Upon return, the variable contains the number of bytes copied if the function succeeds, or the number of bytes required if the buffer was too small.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, use the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -see-also

<a href="/windows/desktop/api/winbase/ns-winbase-commconfig">COMMCONFIG</a>



<a href="/windows/desktop/DevIO/communications-functions">Communications Functions</a>



<a href="/windows/desktop/DevIO/communications-resources">Communications Resources</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setdefaultcommconfiga">SetDefaultCommConfig</a>

## -remarks

> [!NOTE]
> The winbase.h header defines GetDefaultCommConfig as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
