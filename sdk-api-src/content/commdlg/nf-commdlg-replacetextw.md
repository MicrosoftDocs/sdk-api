---
UID: NF:commdlg.ReplaceTextW
title: ReplaceTextW function
author: windows-sdk-content
description: Creates a system-defined modeless dialog box that lets the user specify a string to search for and a replacement string, as well as options to control the find and replace operations.
old-location: dlgbox\replacetext.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxfunctions\replacetext.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ReplaceText, ReplaceText function [Dialog Boxes], ReplaceTextA, ReplaceTextW, _win32_ReplaceText, _win32_replacetext_cpp, commdlg/ReplaceText, commdlg/ReplaceTextA, commdlg/ReplaceTextW, dlgbox.replacetext, winui._win32_replacetext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: commdlg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ReplaceTextW (Unicode) and ReplaceTextA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comdlg32.lib
req.dll: Comdlg32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comdlg32.dll
api_name:
 - ReplaceText
 - ReplaceTextA
 - ReplaceTextW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ReplaceTextW function


## -description


Creates a system-defined modeless dialog box that lets the user specify a string to search for and a replacement string, as well as options to control the find and replace operations.


## -parameters




### -param Arg1 [in, out]

Type: <b>LPFINDREPLACE</b>

A pointer to a <a href="https://msdn.microsoft.com/70ba42bb-3a81-48d5-a117-c234d8106e82">FINDREPLACE</a> structure that contains information used to initialize the dialog box. The dialog box uses this structure to send information about the user's input to your application. For more information, see the following Remarks section.


## -returns



Type: <b>HWND</b>

If the function succeeds, the return value is the window handle to the dialog box. You can use the window handle to communicate with the dialog box or close it.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call the <a href="https://msdn.microsoft.com/20c94a3d-7856-4fa1-86ef-2005b418c0bb">CommDlgExtendedError</a> function, which can return one of the following error codes:




## -remarks



The <b>ReplaceText</b> function does not perform a text replacement operation. Instead, the dialog box sends <a href="https://msdn.microsoft.com/ed0b256a-96df-4588-b8f3-f7d1f89ffe74">FINDMSGSTRING</a> registered messages to the window procedure of the owner window of the dialog box. When you create the dialog box, the  <b>hwndOwner</b> member of the <a href="https://msdn.microsoft.com/70ba42bb-3a81-48d5-a117-c234d8106e82">FINDREPLACE</a> structure is a handle to the owner window.

Before calling <b>ReplaceText</b>, you must call the <a href="https://msdn.microsoft.com/51ddc767-ffce-42bf-885a-24b9ee1b25f0">RegisterWindowMessage</a> function to get the identifier for the <a href="https://msdn.microsoft.com/ed0b256a-96df-4588-b8f3-f7d1f89ffe74">FINDMSGSTRING</a> message. The dialog box procedure uses this identifier to send messages when the user clicks the <b>Find Next</b>, <b>Replace</b>, or <b>Replace All</b> buttons, or when the dialog box is closing. The  <i>lParam</i> parameter of a <b>FINDMSGSTRING</b> message contains a pointer to the <a href="https://msdn.microsoft.com/70ba42bb-3a81-48d5-a117-c234d8106e82">FINDREPLACE</a> structure. The  <b>Flags</b> member of this structure indicates the event that caused the message. Other members of the structure indicate the user's input.

If you create a <b>Replace</b> dialog box, you must also use the <a href="https://msdn.microsoft.com/0afa23a3-f552-40f9-9713-e7bf790ba25c">IsDialogMessage</a> function in the main message loop of your application to ensure that the dialog box correctly processes keyboard input, such as the TAB and ESC keys. The <b>IsDialogMessage</b> function returns a value that indicates whether the Replace dialog box processed the message.

You can provide an <a href="https://msdn.microsoft.com/fe71a71f-9b29-465a-ace4-3c1672613843">FRHookProc</a> hook procedure for a <b>Replace</b> dialog box. The hook procedure can process messages sent to the dialog box. To enable a hook procedure, set the <b>FR_ENABLEHOOK</b> flag in the  <b>Flags</b> member of the <a href="https://msdn.microsoft.com/70ba42bb-3a81-48d5-a117-c234d8106e82">FINDREPLACE</a> structure and specify the address of the hook procedure in the  <b>lpfnHook</b> member.




## -see-also




<a href="https://msdn.microsoft.com/20c94a3d-7856-4fa1-86ef-2005b418c0bb">CommDlgExtendedError</a>



<a href="https://msdn.microsoft.com/28573019-f0bd-4a8e-a1a1-48559f658a81">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/70ba42bb-3a81-48d5-a117-c234d8106e82">FINDREPLACE</a>



<a href="https://msdn.microsoft.com/fe71a71f-9b29-465a-ace4-3c1672613843">FRHookProc</a>



<a href="https://msdn.microsoft.com/0afa23a3-f552-40f9-9713-e7bf790ba25c">IsDialogMessage</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/51ddc767-ffce-42bf-885a-24b9ee1b25f0">RegisterWindowMessage</a>



<a href="https://msdn.microsoft.com/5b90ab3f-b751-486f-a0fa-33f791c31a26">WM_CTLCOLORDLG</a>
 

 

