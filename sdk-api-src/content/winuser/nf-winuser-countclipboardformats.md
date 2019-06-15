---
UID: NF:winuser.CountClipboardFormats
title: CountClipboardFormats function (winuser.h)
author: windows-sdk-content
description: Retrieves the number of different data formats currently on the clipboard.
old-location: dataxchg\countclipboardformats.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\countclipboardformats.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CountClipboardFormats, CountClipboardFormats function [Data Exchange], _win32_CountClipboardFormats, _win32_countclipboardformats_cpp, dataxchg.countclipboardformats, winui._win32_countclipboardformats, winuser/CountClipboardFormats
ms.topic: function
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
 - API-MS-Win-RTCore-NTUser-clipboard-l1-1-0.dll
 - minuser.dll
 - api-ms-win-ntuser-ie-clipboard-l1-1-0.dll
 - ie_stubs.dll
api_name:
 - CountClipboardFormats
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CountClipboardFormats function


## -description


Retrieves the number of different data formats currently on the clipboard. 


## -parameters






## -returns



Type: <b>int</b>

If the function succeeds, the return value is the number of different data formats currently on the clipboard.

If the function fails, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dataxchg/clipboard">Clipboard</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-enumclipboardformats">EnumClipboardFormats</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerclipboardformata">RegisterClipboardFormat</a>
 

 

