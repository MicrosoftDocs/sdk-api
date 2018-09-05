---
UID: NF:winuser.GET_RAWINPUT_CODE_WPARAM
title: GET_RAWINPUT_CODE_WPARAM macro
author: windows-sdk-content
description: Retrieves the input code from wParam in WM_INPUT.
old-location: inputdev\get_rawinput_code_wparam.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputmacros\get_rawinput_code_wparam.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GET_RAWINPUT_CODE_WPARAM, GET_RAWINPUT_CODE_WPARAM macro [Keyboard and Mouse Input], RIM_INPUT, RIM_INPUTSINK, _win32_GET_RAWINPUT_CODE_WPARAM, _win32_get_rawinput_code_wparam_cpp, inputdev.get_rawinput_code_wparam, winui._win32_get_rawinput_code_wparam, winuser/GET_RAWINPUT_CODE_WPARAM
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
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
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - GET_RAWINPUT_CODE_WPARAM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GET_RAWINPUT_CODE_WPARAM macro


## -description


Retrieves the input code from 
			<i>wParam</i> in <a href="https://msdn.microsoft.com/a014d68c-841c-4120-b752-4b3fac60e12d">WM_INPUT</a>.


## -parameters




### -param wParam

Input code. This parameter can be the following value. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RIM_INPUT"></a><a id="rim_input"></a><dl>
<dt><b>RIM_INPUT</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Input occurred while the application was in the foreground. The application must call <a href="https://msdn.microsoft.com/fcc6b242-e152-4364-a977-b0441bec425f">DefWindowProc</a> so the system can perform cleanup.

</td>
</tr>
<tr>
<td width="40%"><a id="RIM_INPUTSINK"></a><a id="rim_inputsink"></a><dl>
<dt><b>RIM_INPUTSINK</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Input occurred while the application was not in the foreground.  The application must call <a href="https://msdn.microsoft.com/fcc6b242-e152-4364-a977-b0441bec425f">DefWindowProc</a> so the system can perform the cleanup.

</td>
</tr>
</table>
 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/ee238c20-c3a5-4b6b-af13-727ea18fb448">RAWINPUT</a>



<a href="https://msdn.microsoft.com/a2afdb80-d68a-4c33-826f-96739d239cd9">Raw Input</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a014d68c-841c-4120-b752-4b3fac60e12d">WM_INPUT</a>
 

 

