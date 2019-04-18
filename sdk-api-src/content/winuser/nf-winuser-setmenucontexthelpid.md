---
UID: NF:winuser.SetMenuContextHelpId
title: SetMenuContextHelpId function (winuser.h)
author: windows-sdk-content
description: Associates a Help context identifier with a menu.
old-location: shell\SetMenuContextHelpId.htm
tech.root: shell
ms.assetid: 55d944db-d889-468a-991a-b9779c90b44f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetMenuContextHelpId, SetMenuContextHelpId function [Windows Shell], _win32_SetMenuContextHelpId, shell.SetMenuContextHelpId, winuser/SetMenuContextHelpId
ms.topic: function
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
api_name:
 - SetMenuContextHelpId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetMenuContextHelpId function


## -description


Associates a Help context identifier with a menu.


## -parameters




### -param arg1

Type: <b>HMENU</b>

A handle to the menu with which to associate the Help context identifier.


### -param arg2

Type: <b>DWORD</b>

The help context identifier.


## -returns



Type: <b>BOOL</b>

Returns nonzero if successful, or zero otherwise.

To retrieve extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



All items in the menu share this identifier. Help context identifiers can't be attached to individual menu items.




## -see-also




<a href="https://msdn.microsoft.com/2b8d3e94-6860-4a75-8373-38afb641eb3b">GetMenuContextHelpId</a>
 

 

