---
UID: NF:commctrl._TrackMouseEvent
title: _TrackMouseEvent function (commctrl.h)
description: Posts messages when the mouse pointer leaves a window or hovers over a window for a specified amount of time. This function calls TrackMouseEvent if it exists, otherwise it emulates it.
helpviewer_keywords: ["_TrackMouseEvent","_TrackMouseEvent function [Keyboard and Mouse Input]","_win32__TrackMouseEvent","_win32__trackmouseevent_cpp","commctrl/_TrackMouseEvent","inputdev._trackmouseevent","winui._win32__trackmouseevent"]
old-location: inputdev\_trackmouseevent.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputfunctions\_trackmouseevent.htm
ms.date: 12/05/2018
ms.keywords: _TrackMouseEvent, _TrackMouseEvent function [Keyboard and Mouse Input], _win32__TrackMouseEvent, _win32__trackmouseevent_cpp, commctrl/_TrackMouseEvent, inputdev._trackmouseevent, winui._win32__trackmouseevent
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TrackMouseEvent
 - commctrl/_TrackMouseEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - _TrackMouseEvent
---

# _TrackMouseEvent function


## -description

Posts messages when the mouse pointer leaves a window or hovers over a window for a specified amount of time. This function calls <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent">TrackMouseEvent</a> if it exists, otherwise it emulates it.

## -parameters

### -param lpEventTrack [in, out]

Type: <b>LPTRACKMOUSEEVENT</b>

A pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-trackmouseevent">TRACKMOUSEEVENT</a> structure that contains tracking information.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, return value is zero.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/inputdev/mouse-input">Mouse Input</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a>



<a href="/windows/desktop/api/winuser/ns-winuser-trackmouseevent">TRACKMOUSEEVENT</a>



<a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent">TrackMouseEvent</a>