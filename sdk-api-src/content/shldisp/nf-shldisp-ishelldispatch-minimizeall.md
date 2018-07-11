---
UID: NF:shldisp.IShellDispatch.MinimizeAll
title: IShellDispatch::MinimizeAll
author: windows-sdk-content
description: Minimizes all of the windows on the desktop. This method has the same effect as right-clicking the taskbar and selecting Minimize All Windows on older systems or clicking the Show Desktop icon on the taskbar.
old-location: shell\IShellDispatch_MinimizeAll.htm
old-project: shell
ms.assetid: 25DD56B0-221E-44a2-9FAD-FB358ADD7FF1
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: IShellDispatch object [Windows Shell],MinimizeAll method, IShellDispatch.MinimizeAll, IShellDispatch::MinimizeAll, MinimizeAll, MinimizeAll method [Windows Shell], MinimizeAll method [Windows Shell],IShellDispatch object, shell.IShellDispatch_MinimizeAll
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
 - IShellDispatch.MinimizeAll
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch::MinimizeAll


## -description


Minimizes all of the windows on the desktop. This method has the same effect as right-clicking the taskbar and selecting <b>Minimize All Windows</b> on older systems or clicking the <b>Show Desktop</b> icon on the taskbar.


## -parameters






## -returns



<h3>JScript</h3>
This method does not return a value.

<h3>VB</h3>
This method does not return a value.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/3af98a16-27d1-4c93-ac72-7c9e24e68c23">Shell.MinimizeAll</a> method.


#### Examples

The following examples show the use of <b>MinimizeAll</b> in use for JScript, VBScript, and Visual Basic.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnShellMinimizeAllJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.MinimizeAll();
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
    function fnShellMinimizeAllVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.MinimizeAll

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
<pre>Private Sub fnShellMinimizeAllVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.MinimizeAll

    Set objShell = Nothing
End Sub
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/9B429C03-7F80-45db-B8CD-58D19FAD2E61">IShellDispatch</a>



<a href="https://msdn.microsoft.com/dcedfa18-6dde-4fb8-9679-4d6ff80249e4">UndoMinimizeALL</a>
 

 

