---
UID: NF:uiautomationcoreapi.WindowPattern_SetWindowVisualState
title: WindowPattern_SetWindowVisualState function (uiautomationcoreapi.h)
description: Sets the visual state of a window; for example, to maximize a window.
helpviewer_keywords: ["WindowPattern_SetWindowVisualState","WindowPattern_SetWindowVisualState function [Windows Accessibility]","uiauto.uiauto_WindowPattern_SetVisualStateConPat","uiauto_WindowPattern_SetVisualStateConPat","uiautomationcoreapi/WindowPattern_SetWindowVisualState","winauto.uiauto_WindowPattern_SetVisualStateConPat"]
old-location: winauto\uiauto_WindowPattern_SetVisualStateConPat.htm
tech.root: WinAuto
ms.assetid: ccd06650-9d37-42b7-bca5-29267c993a40
ms.date: 12/05/2018
ms.keywords: WindowPattern_SetWindowVisualState, WindowPattern_SetWindowVisualState function [Windows Accessibility], uiauto.uiauto_WindowPattern_SetVisualStateConPat, uiauto_WindowPattern_SetVisualStateConPat, uiautomationcoreapi/WindowPattern_SetWindowVisualState, winauto.uiauto_WindowPattern_SetVisualStateConPat
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WindowPattern_SetWindowVisualState
 - uiautomationcoreapi/WindowPattern_SetWindowVisualState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - WindowPattern_SetWindowVisualState
---

# WindowPattern_SetWindowVisualState function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Sets the visual state of a window; for example, to maximize a window.

## -parameters

### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The control pattern object.

### -param state [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-windowvisualstate">WindowVisualState</a></b>

The visual state to set the window to.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.