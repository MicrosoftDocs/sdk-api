---
UID: NF:shldisp.IShellDispatch.UndoMinimizeALL
title: IShellDispatch::UndoMinimizeALL
author: windows-sdk-content
description: Restores all desktop windows to the state they were in before the last MinimizeAll command.
old-location: shell\IShellDispatch_UndoMinimizeALL.htm
old-project: shell
ms.assetid: 32BDE544-C4FF-4a64-99AF-F8960AEC4690
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IShellDispatch object [Windows Shell],UndoMinimizeALL method, IShellDispatch.UndoMinimizeALL, IShellDispatch::UndoMinimizeALL, UndoMinimizeALL, UndoMinimizeALL method [Windows Shell], UndoMinimizeALL method [Windows Shell],IShellDispatch object, shell.IShellDispatch_UndoMinimizeALL
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
 - IShellDispatch.UndoMinimizeALL
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch::UndoMinimizeALL


## -description


Restores all desktop windows to the state they were in before the last <a href="https://msdn.microsoft.com/3af98a16-27d1-4c93-ac72-7c9e24e68c23">MinimizeAll</a> command. This method has the same effect as right-clicking the taskbar and selecting <b>Undo Minimize All Windows</b> (on older systems) or a second clicking of the <b>Show Desktop</b> icon in the taskbar.


## -parameters






## -returns



<h3>JScript</h3>
This method does not return a value.

<h3>VB</h3>
This method does not return a value.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/dcedfa18-6dde-4fb8-9679-4d6ff80249e4">Shell.UndoMinimizeAll</a> method.


#### Examples

The following examples show the use of <b>UndoMinimizeALL</b> in JScript, VBScript, and Visual Basic.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnShellUndoMinimizeALLJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.UndoMinimizeALL();
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
    function fnShellUndoMinimizeALLVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.UndoMinimizeALL

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
<pre>Private Sub fnShellUndoMinimizeAllVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.UndoMinimizeALL

    Set objShell = Nothing
End Sub
</pre>
</td>
</tr>
</table></span></div>


