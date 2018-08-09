---
UID: NF:winuser.SetProcessRestrictionExemption
title: SetProcessRestrictionExemption function
author: windows-sdk-content
description: Exempts the calling process from restrictions preventing desktop processes from interacting with the Windows Store app environment. This function is used by development and debugging tools.
old-location: base\setprocessrestrictionexemption.htm
old-project: procthread
ms.assetid: CC7EE5D7-ADFC-4859-88F8-C5C21AEBF315
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SetProcessRestrictionExemption, SetProcessRestrictionExemption function, base.setprocessrestrictionexemption, winuser/SetProcessRestrictionExemption
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - SetProcessRestrictionExemption
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Any process can call this function, including desktop and Windows Store app processes and processes that use IL code.



