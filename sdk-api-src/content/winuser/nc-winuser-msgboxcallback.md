---
UID: NC:winuser.MSGBOXCALLBACK
title: MSGBOXCALLBACK (winuser.h)
description: A callback function, which you define in your application, that processes help events for the message box.
tech.root: dlgbox
ms.date: 04/14/2021
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: winuser.h
req.idl: 
req.include-header: windows.h
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - winuser.h
api_name:
 - MSGBOXCALLBACK
---

## -description

A callback function, which you define in your application, that processes help events for the message box. The **MSGBOXCALLBACK** type defines a pointer to this callback function. The *MsgBoxCallback* name is a placeholder for the name of the function that you define in your application.

## -parameters

### -param lpHelpInfo

Type: **[LPHELPINFO](/windows/win32/api/winuser/ns-winuser-helpinfo)**

Information about the item for which context-sensitive help has been requested.

## -remarks

## -see-also
