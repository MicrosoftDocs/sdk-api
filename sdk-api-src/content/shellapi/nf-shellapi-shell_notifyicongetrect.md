---
UID: NF:shellapi.Shell_NotifyIconGetRect
title: Shell_NotifyIconGetRect function
author: windows-sdk-content
description: Gets the screen coordinates of the bounding rectangle of a notification icon.
old-location: shell\Shell_NotifyIconGetRect.htm
tech.root: shell
ms.assetid: 81ad13be-a908-4079-b47c-6f983919700b
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: Shell_NotifyIconGetRect, Shell_NotifyIconGetRect function [Windows Shell], _shell_Shell_NotifyIconGetRect, shell.Shell_NotifyIconGetRect, shellapi/Shell_NotifyIconGetRect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - Shell_NotifyIconGetRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Shell_NotifyIconGetRect function


## -description


Gets the screen coordinates of the bounding rectangle of a notification icon.


## -parameters




### -param identifier [in]

Type: <b>const <a href="https://msdn.microsoft.com/2fe4ffba-6fe5-4d34-9cb1-f266e4594b8e">NOTIFYICONIDENTIFIER</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/2fe4ffba-6fe5-4d34-9cb1-f266e4594b8e">NOTIFYICONIDENTIFIER</a> structure that identifies the icon.


### -param iconLocation [out]

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that, when this function returns successfully, receives the coordinates of the icon.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/D37E2BF7-1887-4780-81AD-85B2117321E4">Notifications and the Notification Area</a>
 

 

