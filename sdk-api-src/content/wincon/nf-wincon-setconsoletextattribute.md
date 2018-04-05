---
UID: NF:wincon.SetConsoleTextAttribute
title: SetConsoleTextAttribute function
author: windows-driver-content
description: Sets the attributes of characters written to the console screen buffer by the WriteFile or WriteConsole function, or echoed by the ReadFile or ReadConsole function.
old-location: consoles\setconsoletextattribute.htm
old-project: consoles
ms.assetid: 9fba5bb5-b999-4abd-ab39-7a63d58b8074
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SetConsoleTextAttribute, SetConsoleTextAttribute function [Consoles], _win32_setconsoletextattribute, base.setconsoletextattribute, consoles.setconsoletextattribute, wincon/SetConsoleTextAttribute
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincon.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
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
-	API-MS-Win-Core-Console-l2-1-0.dll
-	KernelBase.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
api_name:
-	SetConsoleTextAttribute
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetConsoleTextAttribute function


## -description


Sets the attributes of characters written to the console screen buffer by the 
<a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a> or 
<a href="https://msdn.microsoft.com/1a13d9ef-75a9-49fd-9717-207f18612b59">WriteConsole</a> function, or echoed by the 
<a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a> or 
<a href="https://msdn.microsoft.com/1aa9ecac-a9b9-4e6d-9206-7a57013de657">ReadConsole</a> function. This function affects text written after the function call.


## -parameters




### -param hConsoleOutput [in]

A handle to the console screen buffer. The handle must have the <b>GENERIC_READ</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/f9a50063-8fc8-4cd1-8f24-9ae3946d3119">Console Buffer Security and Access Rights</a>.


### -param wAttributes [in]

The
						<a href="console_screen_buffers.htm">character attributes</a>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To determine the current color attributes of a screen buffer, call the 
<a href="https://msdn.microsoft.com/eafe819e-a99a-4ce1-8898-8860444a31af">GetConsoleScreenBufferInfo</a> function.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/0226cd94-86d0-452b-80e6-e0fed8af0a62">Using the High-Level Input and Output Functions</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/f94995fc-5f5f-4fcd-969d-7e10020634c2">Console Screen Buffers</a>



<a href="https://msdn.microsoft.com/eafe819e-a99a-4ce1-8898-8860444a31af">GetConsoleScreenBufferInfo</a>



<a href="https://msdn.microsoft.com/1aa9ecac-a9b9-4e6d-9206-7a57013de657">ReadConsole</a>



<a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a>



<a href="https://msdn.microsoft.com/1a13d9ef-75a9-49fd-9717-207f18612b59">WriteConsole</a>



<a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a>
 

 

