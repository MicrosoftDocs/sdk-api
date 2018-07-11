---
UID: NF:shldisp.IShellDispatch.Help
title: IShellDispatch::Help
author: windows-sdk-content
description: Displays the Windows Help and Support window. This method has the same effect as clicking the Start menu and selecting Help and Support.
old-location: shell\IShellDispatch_Help.htm
old-project: shell
ms.assetid: 9460C87E-6703-4df6-A84C-8D394E0E6703
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: Help, Help method [Windows Shell], Help method [Windows Shell],IShellDispatch object, IShellDispatch object [Windows Shell],Help method, IShellDispatch.Help, IShellDispatch::Help, shell.IShellDispatch_Help
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
 - IShellDispatch.Help
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch::Help


## -description


Displays the Windows Help and Support window. This method has the same effect as clicking the <b>Start</b> menu and selecting <b>Help and Support</b>.


## -parameters






## -returns



<h3>JScript</h3>
This method does not return a value.

<h3>VB</h3>
This method does not return a value.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/fc13fef8-dac8-4c59-936d-8da0e63e06d4">Shell.Help</a> method.


#### Examples

The following examples show the use of <b>Help</b> in JScript, VBScript, and Visual Basic.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnShellHelpJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Help();
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
<pre> &lt;script language="VBScript"&gt;
    function fnShellHelpVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Help

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
<pre>Private Sub fnShellHelpVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.Help

    Set objShell = Nothing
End Sub
</pre>
</td>
</tr>
</table></span></div>


