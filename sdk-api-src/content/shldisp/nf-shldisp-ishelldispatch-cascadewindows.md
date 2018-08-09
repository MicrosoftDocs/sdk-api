---
UID: NF:shldisp.IShellDispatch.CascadeWindows
title: IShellDispatch::CascadeWindows
author: windows-sdk-content
description: Cascades all of the windows on the desktop. This method has the same effect as right-clicking the taskbar and selecting Cascade windows.
old-location: shell\IShellDispatch_CascadeWindows.htm
old-project: shell
ms.assetid: 6A957D70-D6A3-4485-8DF3-7FD2C6DEFF78
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CascadeWindows, CascadeWindows method [Windows Shell], CascadeWindows method [Windows Shell],IShellDispatch object, IShellDispatch object [Windows Shell],CascadeWindows method, IShellDispatch.CascadeWindows, IShellDispatch::CascadeWindows, shell.IShellDispatch_CascadeWindows
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellDispatch.CascadeWindows
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch::CascadeWindows


## -description


Cascades all of the windows on the desktop. This method has the same effect as right-clicking the taskbar and selecting <b>Cascade windows</b>.


## -parameters






## -returns



<h3>JScript</h3>
This method does not return a value.

<h3>VB</h3>
This method does not return a value.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/f73d2066-4626-455b-8ee6-f7004cc9e699">Shell.CascadeWindows</a> method.


#### Examples

The following examples show the use of <b>CascadeWindows</b> in JScript, VBScript, and Visual Basic.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnShellCascadeWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.CascadeWindows();
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
    function fnShellCascadeWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.CascadeWindows
        set objShell = nothing
    end function
 &lt;/script&gt;
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
<pre>Private Sub fnShellCascadeWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.CascadeWindows
    Set objShell = Nothing
End Sub
</pre>
</td>
</tr>
</table></span></div>


