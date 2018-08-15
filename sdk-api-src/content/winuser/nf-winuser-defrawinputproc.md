---
UID: NF:winuser.DefRawInputProc
title: DefRawInputProc function
author: windows-sdk-content
description: Calls the default raw input procedure to provide default processing for any raw input messages that an application does not process.
old-location: inputdev\defrawinputproc.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputfunctions\defrawinputproc.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DefRawInputProc, DefRawInputProc function [Keyboard and Mouse Input], _win32_DefRawInputProc, _win32_defrawinputproc_cpp, inputdev.defrawinputproc, winui._win32_defrawinputproc, winuser/DefRawInputProc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - DefRawInputProc
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# DefRawInputProc function


## -description


Calls the default raw input procedure to provide default processing for any raw input messages that an application does not process. This function ensures that every message is processed. <b>DefRawInputProc</b> is called with the same parameters received by the window procedure. 


## -parameters




### -param paRawInput [in]

Type: <b>PRAWINPUT*</b>

An array of <a href="https://msdn.microsoft.com/en-us/library/ms645562(v=VS.85).aspx">RAWINPUT</a> structures. 


### -param nInput [in]

Type: <b>INT</b>

The number of <a href="https://msdn.microsoft.com/en-us/library/ms645562(v=VS.85).aspx">RAWINPUT</a> structures pointed to by 
					<i>paRawInput</i>. 


### -param cbSizeHeader [in]

Type: <b>UINT</b>

The size, in bytes, of the <a href="https://msdn.microsoft.com/en-us/library/ms645571(v=VS.85).aspx">RAWINPUTHEADER</a> structure. 


## -returns



Type: <b>LRESULT</b>

If successful, the function returns <b>S_OK</b>. Otherwise it returns an error value.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms645562(v=VS.85).aspx">RAWINPUT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645571(v=VS.85).aspx">RAWINPUTHEADER</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645536(v=VS.85).aspx">Raw Input</a>



<b>Reference</b>
 

 

