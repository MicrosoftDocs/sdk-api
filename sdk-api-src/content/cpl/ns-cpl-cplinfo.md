---
UID: NS:cpl.tagCPLINFO
title: CPLINFO (cpl.h)
description: Contains resource information and an application-defined value for a dialog box supported by a Control Panel application. (CPLINFO)
helpviewer_keywords: ["*LPCPLINFO","CPLINFO","CPLINFO structure [Windows Shell]","_win32_CPLINFO","cpl/CPLINFO","shell.CPLINFO"]
old-location: shell\CPLINFO.htm
tech.root: shell
ms.assetid: 707950c9-c242-43b2-b665-c97a89e632c5
ms.date: 12/05/2018
ms.keywords: '*LPCPLINFO, CPLINFO, CPLINFO structure [Windows Shell], _win32_CPLINFO, cpl/CPLINFO, shell.CPLINFO'
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
req.typenames: CPLINFO, *LPCPLINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCPLINFO
 - cpl/tagCPLINFO
 - LPCPLINFO
 - cpl/LPCPLINFO
 - CPLINFO
 - cpl/CPLINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Cpl.h
api_name:
 - CPLINFO
---

## -description

Contains resource information and an application-defined value for a dialog box supported by a Control Panel application. The <a href="/windows/desktop/api/cpl/nc-cpl-applet_proc">CPlApplet</a> function of the Control Panel application returns this information to the Control Panel in response to a <a href="/windows/desktop/shell/fa-perceivedtypes">CPL_INQUIRE</a> message.

## -struct-fields

### -field idIcon

Type: <b>int</b>

The resource identifier of the icon that represents the dialog box.

### -field idName

Type: <b>int</b>

The resource identifier of the string containing the short name for the dialog box. This name is intended to be displayed below the icon.

### -field idInfo

Type: <b>int</b>

The resource identifier of the string containing the description for the dialog box that is intended to be displayed when the application icon is selected.

### -field lData

Type: <b>LONG_PTR</b>

A pointer to data defined by the application. When the Control Panel sends the <a href="/windows/desktop/shell/fa-associationarray">CPL_DBLCLK</a> and <a href="/windows/desktop/shell/library-functions-bumper">CPL_STOP</a> messages, it passes this value back to your application.

## -remarks

If the icon or display strings of the dialog box can change based on the state of the computer, you can specify the CPL_DYNAMIC_RES value for the <b>idIcon</b>, <b>idName</b>, or <b>idInfo</b> members rather than specifying a valid resource identifier. This causes the Control Panel to send the <a href="/windows/desktop/shell/glossary">CPL_NEWINQUIRE</a> message each time it needs the icon and display strings. Using this technique is significantly slower, however, because the Control Panel will need to load your application each time it sends the <b>CPL_NEWINQUIRE</b> message.
