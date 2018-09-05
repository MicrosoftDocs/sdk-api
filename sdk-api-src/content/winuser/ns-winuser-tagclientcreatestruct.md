---
UID: NS:winuser.tagCLIENTCREATESTRUCT
title: tagCLIENTCREATESTRUCT
author: windows-sdk-content
description: Contains information about the menu and first multiple-document interface (MDI) child window of an MDI client window.
old-location: winmsg\clientcreatestruct.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowstructures\clientcreatestruct.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPCLIENTCREATESTRUCT, CLIENTCREATESTRUCT, CLIENTCREATESTRUCT structure [Windows and Messages], LPCLIENTCREATESTRUCT, LPCLIENTCREATESTRUCT structure pointer [Windows and Messages], _win32_CLIENTCREATESTRUCT_str, _win32_clientcreatestruct_str_cpp, tagCLIENTCREATESTRUCT, winmsg.clientcreatestruct, winui._win32_clientcreatestruct_str, winuser/CLIENTCREATESTRUCT, winuser/LPCLIENTCREATESTRUCT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: CLIENTCREATESTRUCT, *LPCLIENTCREATESTRUCT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - CLIENTCREATESTRUCT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagCLIENTCREATESTRUCT structure


## -description


Contains information about the menu and first multiple-document interface (MDI) child window of an MDI client window. An application passes a pointer to this structure as the
<i>lpParam</i> parameter of the <a href="https://msdn.microsoft.com/5424b87c-22ea-414e-840e-214d9f0dc9ad">CreateWindow</a> function when creating an MDI client window. 


## -struct-fields




### -field hWindowMenu

Type: <b>HANDLE</b>

A handle to the MDI application's window menu. An MDI application can retrieve this handle from the menu of the MDI frame window by using the <a href="https://msdn.microsoft.com/009ede3f-da6e-4195-90e0-9f046146fd5c">GetSubMenu</a> function. 


### -field idFirstChild

Type: <b>UINT</b>

The child window identifier of the first MDI child window created. The system increments the identifier for each additional MDI child window the application creates, and reassigns identifiers when the application destroys a window to keep the range of identifiers contiguous. These identifiers are used in <a href="https://msdn.microsoft.com/5516098e-fd90-49c8-afb0-78164b028376">WM_COMMAND</a> messages sent to the application's MDI frame window when a child window is chosen from the window menu; they should not conflict with any other command identifiers. 


## -remarks



When the MDI client window is created by calling <a href="https://msdn.microsoft.com/5424b87c-22ea-414e-840e-214d9f0dc9ad">CreateWindow</a>, the system sends a <a href="https://msdn.microsoft.com/d484d0fc-bad0-4fcb-bf4b-37cbc50846ee">WM_CREATE</a> message to the window. The 
				<i>lParam</i> parameter of <b>WM_CREATE</b> contains a pointer to a <a href="https://msdn.microsoft.com/2d67fed4-43de-4151-b124-b710ea64e8a6">CREATESTRUCT</a> structure. The 
				<b>lpCreateParams</b> member of this structure contains a pointer to a <b>CLIENTCREATESTRUCT</b> structure.




## -see-also




<a href="https://msdn.microsoft.com/35dff281-3b11-4954-85cf-a0f1c9ed346a">About the Multiple Document Interface</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/5424b87c-22ea-414e-840e-214d9f0dc9ad">CreateWindow</a>



<a href="https://msdn.microsoft.com/009ede3f-da6e-4195-90e0-9f046146fd5c">GetSubMenu</a>



<a href="https://msdn.microsoft.com/aac21a17-4302-4174-9d72-15366d964094">MDICREATESTRUCT</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/5516098e-fd90-49c8-afb0-78164b028376">WM_COMMAND</a>



<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows</a>
 

 

