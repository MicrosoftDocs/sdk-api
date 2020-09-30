---
UID: NC:cpl.APPLET_PROC
title: APPLET_PROC (cpl.h)
description: Serves as the entry point for a Control Panel application. This is a library-defined callback function.
helpviewer_keywords: ["APPLET_PROC","APPLET_PROC callback","CPlApplet","CPlApplet callback function [Windows Shell]","_win32_CPlApplet","cpl/CPlApplet","shell.CPlApplet"]
old-location: shell\CPlApplet.htm
tech.root: shell
ms.assetid: 23063e34-9d77-4167-83cd-8561accf0a8d
ms.date: 12/05/2018
ms.keywords: APPLET_PROC, APPLET_PROC callback, CPlApplet, CPlApplet callback function [Windows Shell], _win32_CPlApplet, cpl/CPlApplet, shell.CPlApplet
req.header: cpl.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - APPLET_PROC
 - cpl/APPLET_PROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Cpl.h
api_name:
 - CPlApplet
---

## -description

Serves as the entry point for a Control Panel application. This is a library-defined callback function.

## -parameters

### -param hwndCpl

Type: <b>HWND</b>

The identifier of the main window of the controlling application. Use the <i>hwndCPl</i> parameter for dialog boxes or other windows that require a handle to a parent window.

### -param msg

Type: <b>UINT</b>

The message being sent to the Control Panel application.

### -param lParam1

Type: <b>LPARAM</b>

Additional message-specific information.

### -param lParam2

Type: <b>LPARAM</b>

Additional message-specific information.

## -returns

Type: <b>LONG</b>

The return value depends on the message. 

For more information, see the descriptions of the individual <a href="/previous-versions/windows/desktop/legacy/cc144185(v=vs.85)">Control Panel messages</a>.

## -remarks

Implementers of Control Panel items must also implement this function. No default implementation is available.