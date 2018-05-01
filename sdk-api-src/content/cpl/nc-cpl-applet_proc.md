---
UID: NC:cpl.APPLET_PROC
title: APPLET_PROC
author: windows-driver-content
description: Serves as the entry point for a Control Panel application. This is a library-defined callback function.
old-location: shell\CPlApplet.htm
old-project: shell
ms.assetid: 23063e34-9d77-4167-83cd-8561accf0a8d
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: APPLET_PROC, CPlApplet, CPlApplet entry point [Windows Shell], _win32_CPlApplet, cpl/CPlApplet, shell.CPlApplet
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: WMPContextMenuInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Cpl.h
api_name:
-	CPlApplet
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# APPLET_PROC callback


## -description


Serves as the entry point for a Control Panel application. This is a library-defined callback function.


## -parameters




### -param hwndCpl


### -param msg


### -param lParam1

Type: <b>LPARAM</b>

Additional message-specific information.


### -param lParam2

Type: <b>LPARAM</b>

Additional message-specific information.


#### - hwndCPl

Type: <b>HWND</b>

The identifier of the main window of the controlling application. Use the <i>hwndCPl</i> parameter for dialog boxes or other windows that require a handle to a parent window.


#### - uMsg

Type: <b>UINT</b>

The message being sent to the Control Panel application.


## -returns



Type: <b>LONG</b>

The return value depends on the message. 
    					

For more information, see the descriptions of the individual <a href="https://msdn.microsoft.com/2e61cbc0-fbb5-4680-8123-f8ffdcf98210">Control Panel messages</a>.




## -remarks



Implementers of Control Panel items must also implement this function. No default implementation is available.



