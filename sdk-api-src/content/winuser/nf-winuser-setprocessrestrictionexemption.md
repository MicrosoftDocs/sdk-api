---
UID: NF:winuser.SetProcessRestrictionExemption
title: SetProcessRestrictionExemption function (winuser.h)
description: Exempts the calling process from restrictions preventing desktop processes from interacting with the Windows Store app environment. This function is used by development and debugging tools.
helpviewer_keywords: ["SetProcessRestrictionExemption","SetProcessRestrictionExemption function","base.setprocessrestrictionexemption","winuser/SetProcessRestrictionExemption"]
old-location: base\setprocessrestrictionexemption.htm
tech.root: backup
ms.assetid: CC7EE5D7-ADFC-4859-88F8-C5C21AEBF315
ms.date: 12/05/2018
ms.keywords: SetProcessRestrictionExemption, SetProcessRestrictionExemption function, base.setprocessrestrictionexemption, winuser/SetProcessRestrictionExemption
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetProcessRestrictionExemption
 - winuser/SetProcessRestrictionExemption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - ext-ms-win-ntuser-misc-l1-5-1.dll
 - ext-ms-win-ntuser-misc-l1-5-0.dll
 - ext-ms-win-ntuser-misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-2-0.dll
 - ext-ms-win-ntuser-misc-l1-1-0.dll
 - User32.dll
api_name:
 - SetProcessRestrictionExemption
---

# SetProcessRestrictionExemption function


## -description

 Exempts the calling process from restrictions preventing desktop processes from interacting with the Windows Store app environment. This function is used by development and debugging tools.

This function only succeeds if a developer license is present on the system. Once successful the calling process will be able to perform the following actions, subject to User Interface Privilege Isolation (UIPI) restrictions:
<ul>
<li>
Attach global hooks (and event hooks) to Windows Store app processes.

</li>
<li>
Attach input queues between Windows Store app processes, Windows Store app browsers, system processes,  and desktop application processes.

</li>
<li>
Change foreground arbitrarily between the Windows Store app and desktop environments.

</li>
</ul>

## -parameters

### -param fEnableExemption

When set to TRUE, indicates a request to disable exemption for the calling process.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Any process can call this function, including desktop and Windows Store app processes and processes that use IL code.