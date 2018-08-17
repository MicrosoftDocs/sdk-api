---
UID: NF:winuser.GetClipboardViewer
title: GetClipboardViewer function
author: windows-sdk-content
description: Retrieves the handle to the first window in the clipboard viewer chain.
old-location: dataxchg\getclipboardviewer.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\getclipboardviewer.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetClipboardViewer, GetClipboardViewer function [Data Exchange], _win32_GetClipboardViewer, _win32_getclipboardviewer_cpp, dataxchg.getclipboardviewer, winui._win32_getclipboardviewer, winuser/GetClipboardViewer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - GetClipboardViewer
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetClipboardViewer function


## -description


Retrieves the handle to the first window in the clipboard viewer chain.


## -parameters






## -returns



Type: <b>HWND</b>

If the function succeeds, the return value is the handle to the first window in the clipboard viewer chain. 

If there is no clipboard viewer, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/61a9bff7-3c46-4e42-81f7-e020ff0b667f">Clipboard</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/96c06602-05ec-4f38-a53b-1729f2c1ce4f">GetClipboardOwner</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/b1c9c0eb-388f-4fa1-9744-8ebd324cec4f">SetClipboardViewer</a>
 

 

