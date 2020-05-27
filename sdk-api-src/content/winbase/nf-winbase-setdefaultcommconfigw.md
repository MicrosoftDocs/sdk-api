---
UID: NF:winbase.SetDefaultCommConfigW
title: SetDefaultCommConfigW function (winbase.h)
description: Sets the default configuration for a communications device.
helpviewer_keywords: ["SetDefaultCommConfig","SetDefaultCommConfig function","SetDefaultCommConfigA","SetDefaultCommConfigW","_win32_setdefaultcommconfig","base.setdefaultcommconfig","winbase/SetDefaultCommConfig","winbase/SetDefaultCommConfigA","winbase/SetDefaultCommConfigW"]
old-location: base\setdefaultcommconfig.htm
tech.root: devio
ms.assetid: 3b228b56-34ca-4b37-af67-4e4e1fa60df2
ms.date: 12/05/2018
ms.keywords: SetDefaultCommConfig, SetDefaultCommConfig function, SetDefaultCommConfigA, SetDefaultCommConfigW, _win32_setdefaultcommconfig, base.setdefaultcommconfig, winbase/SetDefaultCommConfig, winbase/SetDefaultCommConfigA, winbase/SetDefaultCommConfigW
f1_keywords:
- winbase/SetDefaultCommConfig
dev_langs:
- c++
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetDefaultCommConfigW (Unicode) and SetDefaultCommConfigA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Kernel32.dll
api_name:
- SetDefaultCommConfig
- SetDefaultCommConfigA
- SetDefaultCommConfigW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetDefaultCommConfigW function


## -description


Sets the default configuration for a communications device.


## -parameters




### -param lpszName [in]

The name of the device. For example, COM1 through COM9 are serial ports and LPT1 through LPT9 are parallel ports.


### -param lpCC [in]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-commconfig">COMMCONFIG</a> structure.


### -param dwSize [in]

The size of the structure pointed to by <i>lpCC</i>, in bytes.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-commconfig">COMMCONFIG</a>



<a href="https://docs.microsoft.com/windows/desktop/DevIO/communications-functions">Communications Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/DevIO/communications-resources">Communications Resources</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-getdefaultcommconfiga">GetDefaultCommConfig</a>
 

 

