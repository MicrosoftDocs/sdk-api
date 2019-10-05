---
UID: NF:winuser.DefRawInputProc
title: DefRawInputProc function (winuser.h)
author: windows-sdk-content
description: Calls the default raw input procedure to provide default processing for any raw input messages that an application does not process.
old-location: inputdev\defrawinputproc.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputfunctions\defrawinputproc.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DefRawInputProc, DefRawInputProc function [Keyboard and Mouse Input], _win32_DefRawInputProc, _win32_defrawinputproc_cpp, inputdev.defrawinputproc, winui._win32_defrawinputproc, winuser/DefRawInputProc
ms.topic: function
f1_keywords: 
 - "winuser/DefRawInputProc"
dev_langs:
 - c++
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
 - User32.dll
api_name:
 - DefRawInputProc
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DefRawInputProc function


## -description


Calls the default raw input procedure to provide default processing for any raw input messages that an application does not process. This function ensures that every message is processed. <b>DefRawInputProc</b> is called with the same parameters received by the window procedure. 


## -parameters




### -param paRawInput [in]

Type: <b>PRAWINPUT*</b>

An array of <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-rawinput">RAWINPUT</a> structures. 


### -param nInput [in]

Type: <b>INT</b>

The number of <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-rawinput">RAWINPUT</a> structures pointed to by 
					<i>paRawInput</i>. 


### -param cbSizeHeader [in]

Type: <b>UINT</b>

The size, in bytes, of the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-rawinputheader">RAWINPUTHEADER</a> structure. 


## -returns



Type: <b>LRESULT</b>

If successful, the function returns <b>S_OK</b>. Otherwise it returns an error value.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-rawinput">RAWINPUT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-rawinputheader">RAWINPUTHEADER</a>



<a href="https://docs.microsoft.com/windows/desktop/inputdev/raw-input">Raw Input</a>



<b>Reference</b>
 

 

