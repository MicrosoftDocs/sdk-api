---
UID: NF:winuser.GET_RAWINPUT_CODE_WPARAM
title: GET_RAWINPUT_CODE_WPARAM macro
author: windows-sdk-content
description: Retrieves the input code from wParam in WM_INPUT.
old-location: inputdev\get_rawinput_code_wparam.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputmacros\get_rawinput_code_wparam.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GET_RAWINPUT_CODE_WPARAM, GET_RAWINPUT_CODE_WPARAM macro [Keyboard and Mouse Input], RIM_INPUT, RIM_INPUTSINK, _win32_GET_RAWINPUT_CODE_WPARAM, _win32_get_rawinput_code_wparam_cpp, inputdev.get_rawinput_code_wparam, winui._win32_get_rawinput_code_wparam, winuser/GET_RAWINPUT_CODE_WPARAM
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
---

# GET_RAWINPUT_CODE_WPARAM macro


## -description


Retrieves the input code from 
			<i>wParam</i> in <a href="https://msdn.microsoft.com/en-us/library/ms645590(v=VS.85).aspx">WM_INPUT</a>.


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
Input occurred while the application was in the foreground. The application must call <a href="https://msdn.microsoft.com/en-us/library/ms633572(v=VS.85).aspx">DefWindowProc</a> so the system can perform cleanup.

</td>
</tr>
<tr>
<td width="40%"><a id="RIM_INPUTSINK"></a><a id="rim_inputsink"></a><dl>
<dt><b>RIM_INPUTSINK</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Input occurred while the application was not in the foreground.  The application must call <a href="https://msdn.microsoft.com/en-us/library/ms633572(v=VS.85).aspx">DefWindowProc</a> so the system can perform the cleanup.

</td>
</tr>
</table>
 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms645562(v=VS.85).aspx">RAWINPUT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645536(v=VS.85).aspx">Raw Input</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms645590(v=VS.85).aspx">WM_INPUT</a>
 

 

