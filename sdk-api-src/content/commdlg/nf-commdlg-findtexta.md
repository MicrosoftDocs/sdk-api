---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# FindTextA function


## -description


Creates a system-defined modeless <b>Find</b> dialog box that lets the user specify a string to search for and options to use when searching for text in a document.


## -parameters




### -param Arg1

TBD




#### - lpfr [in]

Type: <b>LPFINDREPLACE</b>

A pointer to a <a href="https://msdn.microsoft.com/70ba42bb-3a81-48d5-a117-c234d8106e82">FINDREPLACE</a> structure that contains information used to initialize the dialog box. The dialog box uses this structure to send information about the user's input to your application. For more information, see the following Remarks section.


## -returns



Type: <b>HWND</b>

If the function succeeds, the return value is the window handle to the dialog box. You can use the window handle to communicate with or to close the dialog box.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call the <a href="https://msdn.microsoft.com/20c94a3d-7856-4fa1-86ef-2005b418c0bb">CommDlgExtendedError</a> function. <b>CommDlgExtendedError</b> may return one of the following error codes: 




## -remarks



The <b>FindText</b> function does not perform a search operation. Instead, the dialog box sends <a href="https://msdn.microsoft.com/ed0b256a-96df-4588-b8f3-f7d1f89ffe74">FINDMSGSTRING</a> registered messages to the window procedure of the owner window of the dialog box. When you create the dialog box, the  <b>hwndOwner</b> member of the <a href="https://msdn.microsoft.com/70ba42bb-3a81-48d5-a117-c234d8106e82">FINDREPLACE</a> structure is a handle to the owner window.

Before calling <b>FindText</b>, you must call the <a href="https://msdn.microsoft.com/51ddc767-ffce-42bf-885a-24b9ee1b25f0">RegisterWindowMessage</a> function to get the identifier for the <a href="https://msdn.microsoft.com/ed0b256a-96df-4588-b8f3-f7d1f89ffe74">FINDMSGSTRING</a> message. The dialog box procedure uses this identifier to send messages when the user clicks the <b>Find Next</b> button, or when the dialog box is closing. The  <i>lParam</i> parameter of the <b>FINDMSGSTRING</b> message contains a pointer to a <a href="https://msdn.microsoft.com/70ba42bb-3a81-48d5-a117-c234d8106e82">FINDREPLACE</a> structure. The  <b>Flags</b> member of this structure indicates the event that caused the message. Other members of the structure indicate the user's input.

If you create a <b>Find</b> dialog box, you must also use the <a href="https://msdn.microsoft.com/0afa23a3-f552-40f9-9713-e7bf790ba25c">IsDialogMessage</a> function in the main message loop of your application to ensure that the dialog box correctly processes keyboard input, such as the TAB and ESC keys. <b>IsDialogMessage</b> returns a value that indicates whether the <b>Find</b> dialog box processed the message.

You can provide an <a href="https://msdn.microsoft.com/fe71a71f-9b29-465a-ace4-3c1672613843">FRHookProc</a> hook procedure for a <b>Find</b> dialog box. The hook procedure can process messages sent to the dialog box. To enable a hook procedure, set the <b>FR_ENABLEHOOK</b> flag in the  <b>Flags</b> member of the <a href="https://msdn.microsoft.com/70ba42bb-3a81-48d5-a117-c234d8106e82">FINDREPLACE</a> structure and specify the address of the hook procedure in the  <b>lpfnHook</b> member.


#### Examples

For an example, see <a href="using_common_dialog_boxes.htm">Finding Text</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/20c94a3d-7856-4fa1-86ef-2005b418c0bb">CommDlgExtendedError</a>



<a href="https://msdn.microsoft.com/28573019-f0bd-4a8e-a1a1-48559f658a81">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/ed0b256a-96df-4588-b8f3-f7d1f89ffe74">FINDMSGSTRING</a>



<a href="https://msdn.microsoft.com/70ba42bb-3a81-48d5-a117-c234d8106e82">FINDREPLACE</a>



<a href="https://msdn.microsoft.com/fe71a71f-9b29-465a-ace4-3c1672613843">FRHookProc</a>



<a href="https://msdn.microsoft.com/0afa23a3-f552-40f9-9713-e7bf790ba25c">IsDialogMessage</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/51ddc767-ffce-42bf-885a-24b9ee1b25f0">RegisterWindowMessage</a>



<a href="https://msdn.microsoft.com/6044373d-1d5b-4941-a9a0-5e2e86232593">ReplaceText</a>
 

 

