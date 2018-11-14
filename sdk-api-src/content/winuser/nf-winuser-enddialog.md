---
UID: NF:winuser.EndDialog
title: EndDialog function
author: windows-sdk-content
description: Destroys a modal dialog box, causing the system to end any processing for the dialog box.
old-location: dlgbox\enddialog.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\enddialog.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: EndDialog, EndDialog function [Dialog Boxes], _win32_EndDialog, _win32_enddialog_cpp, dlgbox.enddialog, winui._win32_enddialog, winuser/EndDialog
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - Ext-MS-Win-NTUser-DialogBox-l1-1-0.dll
 - Ext-MS-Win-NTUser-DialogBox-l1-1-1.dll
 - ext-ms-win-ntuser-dialogbox-l1-1-2.dll
api_name:
 - EndDialog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- EndDialog
: 
---

# EndDialog function


## -description


Destroys a modal dialog box, causing the system to end any processing for the dialog box. 


## -parameters




### -param hDlg [in]

Type: <b>HWND</b>

A handle to the dialog box to be destroyed. 


### -param nResult [in]

Type: <b>INT_PTR</b>

The value to be returned to the application from the function that created the dialog box. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Dialog boxes created by the <a href="https://msdn.microsoft.com/0b28b084-e519-4114-9950-0aebf089b0c8">DialogBox</a>, <a href="https://msdn.microsoft.com/f6d6b80b-251f-44a0-9deb-e518af170b14">DialogBoxParam</a>, <a href="https://msdn.microsoft.com/0af783b3-804d-4075-8046-5109f37e275d">DialogBoxIndirect</a>, and <a href="https://msdn.microsoft.com/ce241d7b-8775-4c0d-bb4b-87df5f58f8a8">DialogBoxIndirectParam</a> functions must be destroyed using the <b>EndDialog</b> function. An application calls <b>EndDialog</b> from within the dialog box procedure; the function must not be used for any other purpose. 

A dialog box procedure can call <b>EndDialog</b> at any time, even during the processing of the <a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a> message. If your application calls the function while <b>WM_INITDIALOG</b> is being processed, the dialog box is destroyed before it is shown and before the input focus is set. 

<b>EndDialog</b> does not destroy the dialog box immediately. Instead, it sets a flag and allows the dialog box procedure to return control to the system. The system checks the flag before attempting to retrieve the next message from the application queue. If the flag is set, the system ends the message loop, destroys the dialog box, and uses the value in <i>nResult</i> as the return value from the function that created the dialog box. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/07ebee3c-5aa7-4b0d-b6cb-e642e01e1a88">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/0b28b084-e519-4114-9950-0aebf089b0c8">DialogBox</a>



<a href="https://msdn.microsoft.com/0af783b3-804d-4075-8046-5109f37e275d">DialogBoxIndirect</a>



<a href="https://msdn.microsoft.com/ce241d7b-8775-4c0d-bb4b-87df5f58f8a8">DialogBoxIndirectParam</a>



<a href="https://msdn.microsoft.com/f6d6b80b-251f-44a0-9deb-e518af170b14">DialogBoxParam</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a>
 

 

