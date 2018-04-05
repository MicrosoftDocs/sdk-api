---
UID: NF:wincon.GetNumberOfConsoleMouseButtons
title: GetNumberOfConsoleMouseButtons function
author: windows-driver-content
description: Retrieves the number of buttons on the mouse used by the current console.
old-location: consoles\getnumberofconsolemousebuttons.htm
old-project: consoles
ms.assetid: 78a6a3be-b42f-4a7a-a612-b6a2019cfec2
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetNumberOfConsoleMouseButtons, GetNumberOfConsoleMouseButtons function [Consoles], _win32_getnumberofconsolemousebuttons, base.getnumberofconsolemousebuttons, consoles.getnumberofconsolemousebuttons, wincon/GetNumberOfConsoleMouseButtons
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincon.h
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
req.typenames: WICMetadataPattern
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
api_name:
-	GetNumberOfConsoleMouseButtons
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetNumberOfConsoleMouseButtons function


## -description


Retrieves the number of buttons on the mouse used by the current console.


## -parameters




### -param lpNumberOfMouseButtons [out]

A pointer to a variable that receives the number of mouse buttons.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



When a console receives mouse input, an 
<a href="https://msdn.microsoft.com/a46ba7fd-097a-455d-96ac-13aa01e11dc1">INPUT_RECORD</a> structure containing a 
<a href="https://msdn.microsoft.com/84ea54c6-8872-4111-8d72-1377409b9247">MOUSE_EVENT_RECORD</a> structure is placed in the console's input buffer. The <b>dwButtonState</b> member of 
<b>MOUSE_EVENT_RECORD</b> has a bit indicating the state of each mouse button. The bit is 1 if the button is down and 0 if the button is up. To determine the number of bits that are significant, use 
<b>GetNumberOfConsoleMouseButtons</b>.




## -see-also




<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/6e536658-8a27-478e-82ee-d1e11f351301">Console Input Buffer</a>



<a href="https://msdn.microsoft.com/a46ba7fd-097a-455d-96ac-13aa01e11dc1">INPUT_RECORD</a>



<a href="https://msdn.microsoft.com/84ea54c6-8872-4111-8d72-1377409b9247">MOUSE_EVENT_RECORD</a>



<a href="https://msdn.microsoft.com/5a9f7b18-cdea-4041-a377-5532d30e0105">ReadConsoleInput</a>
 

 

