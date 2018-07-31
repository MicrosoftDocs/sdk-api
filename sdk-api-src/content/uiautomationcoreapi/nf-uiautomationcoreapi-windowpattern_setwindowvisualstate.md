---
UID: NF:uiautomationcoreapi.WindowPattern_SetWindowVisualState
title: WindowPattern_SetWindowVisualState function
author: windows-sdk-content
description: Sets the visual state of a window; for example, to maximize a window.
old-location: winauto\uiauto_WindowPattern_SetVisualStateConPat.htm
old-project: WinAuto
ms.assetid: ccd06650-9d37-42b7-bca5-29267c993a40
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WindowPattern_SetWindowVisualState, WindowPattern_SetWindowVisualState function [Windows Accessibility], uiauto.uiauto_WindowPattern_SetVisualStateConPat, uiauto_WindowPattern_SetVisualStateConPat, uiautomationcoreapi/WindowPattern_SetWindowVisualState, winauto.uiauto_WindowPattern_SetVisualStateConPat
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - WindowPattern_SetWindowVisualState
product: Windows
targetos: Windows
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# WindowPattern_SetWindowVisualState function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Sets the visual state of a window; for example, to maximize a window.


## -parameters




### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The control pattern object.


### -param state [in]

Type: <b><a href="https://msdn.microsoft.com/5912551c-2745-434b-98de-bf24212f7eef">WindowVisualState</a></b>

The visual state to set the window to.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.



