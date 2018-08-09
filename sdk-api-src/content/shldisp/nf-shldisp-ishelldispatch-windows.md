---
UID: NF:shldisp.IShellDispatch.Windows
title: IShellDispatch::Windows
author: windows-sdk-content
description: Creates and returns a ShellWindows object. This object represents a collection of all of the open windows that belong to the Shell.
old-location: shell\IShellDispatch_Windows.htm
old-project: shell
ms.assetid: 788E2106-3534-4e22-801F-677FD02BDFE0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IShellDispatch object [Windows Shell],Windows method, IShellDispatch.Windows, IShellDispatch::Windows, Windows, Windows method [Windows Shell], Windows method [Windows Shell],IShellDispatch object, shell.IShellDispatch_Windows
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
 - IShellDispatch.Windows
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch::Windows


## -description


Creates and returns a <a href="https://msdn.microsoft.com/cad1f961-7fb4-4ba1-be48-b664d3de2c60">ShellWindows</a> object. This object represents a collection of all of the open windows that belong to the Shell.


## -parameters




### -param ppid






## -returns



<h3>JScript</h3>
Type: <b><a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>**</b>

An object reference to the <a href="https://msdn.microsoft.com/cad1f961-7fb4-4ba1-be48-b664d3de2c60">ShellWindows</a> object.

<h3>VB</h3>
Type: <b><a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>**</b>

An object reference to the <a href="https://msdn.microsoft.com/cad1f961-7fb4-4ba1-be48-b664d3de2c60">ShellWindows</a> object.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/ffa6311c-8bbe-45c4-9b06-069779d2306d">Shell.Windows</a> method.


#### Examples

The following examples use <b>Windows</b> to retrieve the <a href="https://msdn.microsoft.com/cad1f961-7fb4-4ba1-be48-b664d3de2c60">ShellWindows</a> object and display a count of the number of items that it contains. Usage is shown for JScript, VBScript, and Visual Basic.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnShellWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Windows();

        if (objShellWindows != null)
        {
            alert(objShellWindows.Count);
        }
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
    function fnShellWindowsVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Windows

        if (not objShellWindows is nothing) then
            alert(objShellWindows.Count)
        end if

        set objShellWindows = nothing
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
<pre>Private Sub fnShellWindowsVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
</pre>
</td>
</tr>
</table></span></div>


