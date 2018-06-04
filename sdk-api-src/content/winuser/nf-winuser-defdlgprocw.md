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

# DefDlgProcW function


## -description


Calls the default dialog box window procedure to provide default processing for any window messages that a dialog box with a private window class does not process. 


## -parameters




### -param hDlg [in]

Type: <b>HWND</b>

A handle to the dialog box. 


### -param Msg [in]

Type: <b>UINT</b>

The message. 


### -param wParam [in]

Type: <b>WPARAM</b>

Additional message-specific information. 


### -param lParam [in]

Type: <b>LPARAM</b>

Additional message-specific information. 


## -returns



Type: <b>LRESULT</b>

The return value specifies the result of the message processing and depends on the message sent.




## -remarks



The <b>DefDlgProc</b> function is the window procedure for the predefined class of dialog box. This procedure provides internal processing for the dialog box by forwarding messages to the dialog box procedure and carrying out default processing for any messages that the dialog box procedure returns as <b>FALSE</b>. Applications that create custom window procedures for their custom dialog boxes often use <b>DefDlgProc</b> instead of the <a href="https://msdn.microsoft.com/fcc6b242-e152-4364-a977-b0441bec425f">DefWindowProc</a> function to carry out default message processing. 

Applications create custom dialog box classes by filling a <a href="https://msdn.microsoft.com/7e2a4e89-19b6-4ef7-81dd-f44a3874e546">WNDCLASS</a> structure with appropriate information and registering the class with the <a href="https://msdn.microsoft.com/485115e5-b4ec-4e93-89ce-eee229ccabb7">RegisterClass</a> function. Some applications fill the structure by using the <a href="https://msdn.microsoft.com/f7eb12c9-ff24-465d-8c6d-8ee5777c05bc">GetClassInfo</a> function, specifying the name of the predefined dialog box. In such cases, the applications modify at least the <b>lpszClassName</b> member before registering. In all cases, the <b>cbWndExtra</b> member of <b>WNDCLASS</b> for a custom dialog box class must be set to at least <b>DLGWINDOWEXTRA</b>.

The <b>DefDlgProc</b> function must not be called by a dialog box procedure; doing so results in recursive execution. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/fcc6b242-e152-4364-a977-b0441bec425f">DefWindowProc</a>



<a href="https://msdn.microsoft.com/07ebee3c-5aa7-4b0d-b6cb-e642e01e1a88">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/f7eb12c9-ff24-465d-8c6d-8ee5777c05bc">GetClassInfo</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/485115e5-b4ec-4e93-89ce-eee229ccabb7">RegisterClass</a>



<a href="https://msdn.microsoft.com/7e2a4e89-19b6-4ef7-81dd-f44a3874e546">WNDCLASS</a>
 

 

