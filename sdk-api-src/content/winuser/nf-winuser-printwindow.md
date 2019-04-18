---
UID: NF:winuser.PrintWindow
title: PrintWindow function (winuser.h)
author: windows-sdk-content
description: The PrintWindow function copies a visual window into the specified device context (DC), typically a printer DC.
old-location: gdi\printwindow.htm
tech.root: printdocs
ms.assetid: 00b38cd8-1cfb-408e-88da-6e61563d9d8e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PW_CLIENTONLY, PrintWindow, PrintWindow function [Windows GDI], _win32_PrintWindow, gdi.printwindow, winuser/PrintWindow
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
 - ext-ms-win-ntuser-draw-l1-1-2.dll
api_name:
 - PrintWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PrintWindow function


## -description


The <b>PrintWindow</b> function copies a visual window into the specified device context (DC), typically a printer DC.


## -parameters




### -param hwnd

A handle to the window that will be copied.


### -param hdcBlt

A handle to the device context.


### -param nFlags

The drawing options. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PW_CLIENTONLY"></a><a id="pw_clientonly"></a><dl>
<dt><b>PW_CLIENTONLY</b></dt>
</dl>
</td>
<td width="60%">
Only the client area of the window is copied to <i>hdcBlt</i>. By default, the entire window is copied.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, it returns a nonzero value.

If the function fails, it returns zero.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The application that owns the window referenced by hWnd processes the <b>PrintWindow</b> call and renders the image in the device context that is referenced by <i>hdcBlt</i>. The application  receives a <a href="https://msdn.microsoft.com/e6be2ecd-603a-405f-8a48-68d971e1f6de">WM_PRINT</a> message or, if the <b>PW_PRINTCLIENT</b> flag is specified, a <a href="https://msdn.microsoft.com/8703ee74-812a-4ca2-8ee3-a3b8779739e7">WM_PRINTCLIENT</a> message.
For more information, see <b>WM_PRINT</b> and <b>WM_PRINTCLIENT</b>.





## -see-also




<a href="https://msdn.microsoft.com/ff1f72d2-163d-40c4-ab65-f406f9b78a84">Painting and Drawing Messages</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>



<a href="https://msdn.microsoft.com/e6be2ecd-603a-405f-8a48-68d971e1f6de">WM_PRINT</a>



<a href="https://msdn.microsoft.com/8703ee74-812a-4ca2-8ee3-a3b8779739e7">WM_PRINTCLIENT</a>
 

 

