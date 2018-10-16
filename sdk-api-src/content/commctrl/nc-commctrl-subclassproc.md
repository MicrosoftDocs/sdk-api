---
UID: NC:commctrl.SUBCLASSPROC
title: SUBCLASSPROC
author: windows-sdk-content
description: Defines the prototype for the callback function used by RemoveWindowSubclass and SetWindowSubclass.
old-location: shell\SUBCLASSPROC_Function.htm
tech.root: shell
ms.assetid: 44e4cbe0-8252-4bcc-885e-d8af856e8ad7
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: SUBCLASSPROC, SUBCLASSPROC callback, SUBCLASSPROC callback function [Windows Shell], commctrl/SUBCLASSPROC, inet_SUBCLASSPROC_Function, shell.SUBCLASSPROC_Function
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: commctrl.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Commctrl.h
api_name:
 - SUBCLASSPROC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SUBCLASSPROC callback function


## -description


Defines the prototype for the callback function used by <a href="https://msdn.microsoft.com/09f27240-f3af-4791-afcb-a82bda79712a">RemoveWindowSubclass</a> and <a href="https://msdn.microsoft.com/0b11144d-eb4e-462c-96d3-38c4bac48f2a">SetWindowSubclass</a>.


## -parameters




### -param hWnd

Type: <b>HWND</b>

The handle to the subclassed window.


### -param uMsg

Type: <b>UINT</b>

The message being passed.


### -param wParam

Type: <b>WPARAM</b>

Additional message information. The contents of this parameter depend on the value of <i>uMsg</i>.


### -param lParam

Type: <b>LPARAM</b>

Additional message information. The contents of this parameter depend on the value of <i>uMsg</i>.


### -param uIdSubclass

Type: <b>UINT_PTR</b>

The subclass ID.


### -param dwRefData

Type: <b>DWORD_PTR</b>

The reference data provided to the <a href="https://msdn.microsoft.com/0b11144d-eb4e-462c-96d3-38c4bac48f2a">SetWindowSubclass</a> function. This can be used to associate the subclass instance with a "this" pointer.


## -returns



Type: <b>LRESULT</b>

The return value is the result of the message processing and depends on the message sent.



