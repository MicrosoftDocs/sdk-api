---
UID: NF:shldisp.IShellDispatch.SetTime
title: IShellDispatch::SetTime
author: windows-driver-content
description: Displays the Date and Time dialog box. This method has the same effect as right-clicking the clock in the taskbar status area and selecting Adjust date/time.
old-location: shell\IShellDispatch_SetTime.htm
old-project: shell
ms.assetid: D4B949F6-5508-4624-9706-491184703DC6
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: IShellDispatch object [Windows Shell],SetTime method, IShellDispatch.SetTime, IShellDispatch::SetTime, SetTime, SetTime method [Windows Shell], SetTime method [Windows Shell],IShellDispatch object, shell.IShellDispatch_SetTime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IShellDispatch.SetTime
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch::SetTime


## -description


Displays the <b>Date and Time</b> dialog box. This method has the same effect as right-clicking the clock in the taskbar status area and selecting <b>Adjust date/time</b>.


## -parameters






## -returns



<h3>JScript</h3>
This method does not return a value.

<h3>VB</h3>
This method does not return a value.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/01694607-3fc2-4d0d-ba48-5bdbb40da000">Shell.SetTime</a> method.


#### Examples

The following examples show the use of <b>SetTime</b> in JScript, VBScript, and Visual Basic.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnShellSetTimeJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.SetTime();
    }
&lt;/script&gt;
</pre>
</td>
</tr>
</table></span></div>
VBScript:

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>&lt;script language="VBScript"&gt;
    function fnShellSetTimeVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.SetTime
 
        set objShell = nothing
    end function
</pre>
</td>
</tr>
</table></span></div>
Visual Basic:

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Private Sub fnShellSetTimeVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.SetTime
 
    Set objShell = Nothing
</pre>
</td>
</tr>
</table></span></div>


