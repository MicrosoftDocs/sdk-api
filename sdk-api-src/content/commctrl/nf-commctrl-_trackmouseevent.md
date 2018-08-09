---
UID: NF:commctrl._TrackMouseEvent
title: "_TrackMouseEvent function"
author: windows-sdk-content
description: Posts messages when the mouse pointer leaves a window or hovers over a window for a specified amount of time. This function calls TrackMouseEvent if it exists, otherwise it emulates it.
old-location: inputdev\_trackmouseevent.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputfunctions\_trackmouseevent.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "_TrackMouseEvent, _TrackMouseEvent function [Keyboard and Mouse Input], _win32__TrackMouseEvent, _win32__trackmouseevent_cpp, commctrl/_TrackMouseEvent, inputdev._trackmouseevent, winui._win32__trackmouseevent"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - _TrackMouseEvent
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
---

# _TrackMouseEvent function


## -description


Posts messages when the mouse pointer leaves a window or hovers over a window for a specified amount of time. This function calls <a href="https://msdn.microsoft.com/en-us/library/ms646265(v=VS.85).aspx">TrackMouseEvent</a> if it exists, otherwise it emulates it.


## -parameters




### -param lpEventTrack [in, out]

Type: <b>LPTRACKMOUSEEVENT</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms645604(v=VS.85).aspx">TRACKMOUSEEVENT</a> structure that contains tracking information. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, return value is zero.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms645533(v=VS.85).aspx">Mouse Input</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645604(v=VS.85).aspx">TRACKMOUSEEVENT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646265(v=VS.85).aspx">TrackMouseEvent</a>
 

 

