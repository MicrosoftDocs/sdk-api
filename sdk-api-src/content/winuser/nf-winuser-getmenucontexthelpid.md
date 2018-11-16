---
UID: NF:winuser.GetMenuContextHelpId
title: GetMenuContextHelpId function
author: windows-sdk-content
description: Retrieves the Help context identifier associated with the specified menu.
old-location: shell\GetMenuContextHelpId.htm
tech.root: shell
ms.assetid: 2b8d3e94-6860-4a75-8373-38afb641eb3b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetMenuContextHelpId, GetMenuContextHelpId function [Windows Shell], _win32_GetMenuContextHelpId, shell.GetMenuContextHelpId, winuser/GetMenuContextHelpId
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - GetMenuContextHelpId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetMenuContextHelpId
: 
---

# GetMenuContextHelpId function


## -description


Retrieves the Help context identifier associated with the specified menu.


## -parameters




### -param Arg1

Type: <b>HMENU</b>

A handle to the menu for which the Help context identifier is to be retrieved.


## -returns



Type: <b>DWORD</b>

Returns the Help context identifier if the menu has one, or zero otherwise.




## -see-also




<a href="https://msdn.microsoft.com/55d944db-d889-468a-991a-b9779c90b44f">SetMenuContextHelpId</a>
 

 

