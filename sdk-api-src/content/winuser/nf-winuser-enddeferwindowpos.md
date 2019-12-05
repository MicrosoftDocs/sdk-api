---
UID: NF:winuser.EndDeferWindowPos
title: EndDeferWindowPos function (winuser.h)
description: Simultaneously updates the position and size of one or more windows in a single screen-refreshing cycle.
old-location: winmsg\enddeferwindowpos.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\enddeferwindowpos.htm
ms.date: 12/05/2018
ms.keywords: EndDeferWindowPos, EndDeferWindowPos function [Windows and Messages], _win32_EndDeferWindowPos, _win32_enddeferwindowpos_cpp, winmsg.enddeferwindowpos, winui._win32_enddeferwindowpos, winuser/EndDeferWindowPos
ms.topic: function
f1_keywords:
- winuser/EndDeferWindowPos
dev_langs:
- c++
req.header: winuser.h
req.include-header: Windows.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- User32.dll
- API-MS-Win-NTUser-IE-Window-l1-1-0.dll
- ie_shims.dll
- API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
- minuser.dll
- Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
api_name:
- EndDeferWindowPos
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EndDeferWindowPos function


## -description


Simultaneously updates the position and size of one or more windows in a single screen-refreshing cycle. 


## -parameters




### -param hWinPosInfo [in]

Type: <b>HDWP</b>

A handle to a multiple-window 
					– position structure that contains size and position information for one or more windows. This internal structure is returned by the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-begindeferwindowpos">BeginDeferWindowPos</a> function or by the most recent call to the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-deferwindowpos">DeferWindowPos</a> function. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 




## -remarks



The <b>EndDeferWindowPos</b> function sends the <a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-windowposchanging">WM_WINDOWPOSCHANGING</a> and <a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-windowposchanged">WM_WINDOWPOSCHANGED</a> messages to each window identified in the internal structure. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-begindeferwindowpos">BeginDeferWindowPos</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-deferwindowpos">DeferWindowPos</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-windowposchanged">WM_WINDOWPOSCHANGED</a>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-windowposchanging">WM_WINDOWPOSCHANGING</a>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/windows">Windows</a>
 

 

