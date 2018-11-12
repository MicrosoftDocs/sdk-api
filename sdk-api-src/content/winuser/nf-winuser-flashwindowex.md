---
UID: NF:winuser.FlashWindowEx
title: FlashWindowEx function
author: windows-sdk-content
description: Flashes the specified window. It does not change the active state of the window.
old-location: base\flashwindowex.htm
tech.root: debug
ms.assetid: 474ec2d9-3ee9-4622-843e-d6ae36fedd7f
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: FlashWindowEx, FlashWindowEx function, _win32_flashwindowex, base.flashwindowex, winuser/FlashWindowEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - FlashWindowEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FlashWindowEx function


## -description


Flashes the specified window. It does not change the active state of the window.


## -parameters




### -param pfwi [in]

A pointer to a 
<a href="https://msdn.microsoft.com/b16636bc-fa77-4eb9-9801-dc2cdf0556e5">FLASHWINFO</a> structure.


## -returns



The return value specifies the window's state before the call to the 
<b>FlashWindowEx</b> function. If the window caption was drawn as active before the call, the return value is nonzero. Otherwise, the return value is zero.




## -remarks



Typically, you flash a window to inform the user that the window requires attention but does not currently have the keyboard focus. When a window flashes, it appears to change from inactive to active status. An inactive caption bar changes to an active caption bar; an active caption bar changes to an inactive caption bar.




## -see-also




<a href="https://msdn.microsoft.com/ae8ad3a2-1f1a-46d6-adaa-74c50c07dcc5">Error Handling Functions</a>



<a href="https://msdn.microsoft.com/b16636bc-fa77-4eb9-9801-dc2cdf0556e5">FLASHWINFO</a>



<a href="https://msdn.microsoft.com/35b6e93c-323a-4592-9394-a2e9dd79d9e6">Notifying the User</a>
 

 

