---
UID: NF:uiautomationcoreapi.UiaEventAddWindow
title: UiaEventAddWindow function
author: windows-sdk-content
description: Adds a window to the event listener.
old-location: winauto\uiauto_UiaEventAddWindowFunction.htm
tech.root: WinAuto
ms.assetid: 1044dbe0-1b66-41f4-916d-eb23c0a0c92b
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: UiaEventAddWindow, UiaEventAddWindow function [Windows Accessibility], uiauto.uiauto_UiaEventAddWindowFunction, uiauto_UiaEventAddWindowFunction, uiautomationcoreapi/UiaEventAddWindow, winauto.uiauto_UiaEventAddWindowFunction
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: uiautomationcoreapi.h
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
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - UiaEventAddWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaEventAddWindow function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Adds a window to the event listener.


## -parameters




### -param hEvent [in]

Type: <b>HUIAEVENT</b>

The event being listened for. This event was retrieved from <a href="https://msdn.microsoft.com/6d53c864-2791-4693-84dd-c7c1d8262b1f">UiaAddEvent</a>.


### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The handle of the window to add.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.



