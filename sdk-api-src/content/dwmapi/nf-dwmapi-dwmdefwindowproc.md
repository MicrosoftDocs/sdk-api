---
UID: NF:dwmapi.DwmDefWindowProc
title: DwmDefWindowProc function
author: windows-sdk-content
description: Default window procedure for Desktop Window Manager (DWM) hit testing within the non-client area.
old-location: dwm\dwmdefwindowproc.htm
old-project: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmdefwindowproc.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DwmDefWindowProc, DwmDefWindowProc function [Desktop Window Manager], _udwm_dwmdefwindowproc, _udwm_dwmdefwindowproc_cpp, dwm.dwmdefwindowproc, dwmapi/DwmDefWindowProc, winui._udwm_dwmdefwindowproc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dwmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Dwmapi.dll
 - ext-ms-win-dwmapi-ext-l1-1-0.dll
api_name:
 - DwmDefWindowProc
product: Windows
targetos: Windows
req.lib: Dwmapi.lib
req.dll: Dwmapi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DwmDefWindowProc function


## -description


Default window procedure for Desktop Window Manager (DWM) hit testing within the non-client area.

You also need to ensure that <b>DwmDefWindowProc</b> is called for the <a href="https://msdn.microsoft.com/b3ada6db-93ce-45d7-b408-d08692328aeb">WM_NCMOUSELEAVE</a> message. If <b>DwmDefWindowProc</b> is not called for the <b>WM_NCMOUSELEAVE</b> message, DWM does not remove the highlighting from the <b>Maximize</b>, <b>Minimize</b>, and <b>Close</b> buttons when the cursor leaves the window.


## -parameters




### -param hWnd [in]

A handle to the window procedure that received the message.


### -param msg

The message.


### -param wParam

Specifies additional message information. The content of this parameter depends on the value of the <i>msg</i> parameter.


### -param lParam

Specifies additional message information. The content of this parameter depends on the value of the <i>msg</i> parameter.


### -param plResult [out]

A pointer to an <b>LRESULT</b> value that, when this method returns successfully,receives the result of the hit test.


## -returns



<b>TRUE</b> if <b>DwmDefWindowProc</b> handled the message; otherwise, <b>FALSE</b>.




## -remarks



When creating custom frames that include the standard caption buttons, <a href="https://msdn.microsoft.com/4c860466-a9f8-4af8-96b9-cee005481875">WM_NCHITTEST</a> and other non-client hit test messages should first be passed to the <b>DwmDefWindowProc</b> function. This enables the DWM to provide hit testing for the captions buttons. If <b>DwmDefWindowProc</b> does not handle the non-client hit test messages, further processing of these messages might be neccessary.



