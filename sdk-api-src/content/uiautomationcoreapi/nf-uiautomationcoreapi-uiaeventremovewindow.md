---
UID: NF:uiautomationcoreapi.UiaEventRemoveWindow
title: UiaEventRemoveWindow function (uiautomationcoreapi.h)
description: Removes a window from the event listener.
helpviewer_keywords: ["UiaEventRemoveWindow","UiaEventRemoveWindow function [Windows Accessibility]","uiauto.uiauto_UiaEventRemoveWindowFunction","uiauto_UiaEventRemoveWindowFunction","uiautomationcoreapi/UiaEventRemoveWindow","winauto.uiauto_UiaEventRemoveWindowFunction"]
old-location: winauto\uiauto_UiaEventRemoveWindowFunction.htm
tech.root: WinAuto
ms.assetid: 5c989cbf-b55a-4576-bacc-6e9955d4707f
ms.date: 12/05/2018
ms.keywords: UiaEventRemoveWindow, UiaEventRemoveWindow function [Windows Accessibility], uiauto.uiauto_UiaEventRemoveWindowFunction, uiauto_UiaEventRemoveWindowFunction, uiautomationcoreapi/UiaEventRemoveWindow, winauto.uiauto_UiaEventRemoveWindowFunction
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
 - UiaEventRemoveWindow
 - uiautomationcoreapi/UiaEventRemoveWindow
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
 - UiaEventRemoveWindow
---

# UiaEventRemoveWindow function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Removes a window from the event listener.

## -parameters

### -param hEvent [in]

Type: <b>HUIAEVENT</b>

The event being listened for. This event was retrieved from <a href="/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaaddevent">UiaAddEvent</a>.

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The handle of the window to remove.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.