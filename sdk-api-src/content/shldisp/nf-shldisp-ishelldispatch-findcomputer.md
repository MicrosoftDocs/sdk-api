---
UID: NF:shldisp.IShellDispatch.FindComputer
title: IShellDispatch::FindComputer
author: windows-sdk-content
description: Displays the Search Results:\_Computers dialog box. The dialog box shows the result of the search for a specified computer.
old-location: shell\IShellDispatch_FindComputer.htm
old-project: shell
ms.assetid: 9B687A8A-BB29-49a0-8AE3-11A75FAF3257
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: FindComputer, FindComputer method [Windows Shell], FindComputer method [Windows Shell],IShellDispatch object, IShellDispatch object [Windows Shell],FindComputer method, IShellDispatch.FindComputer, IShellDispatch::FindComputer, shell.IShellDispatch_FindComputer
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
 - IShellDispatch.FindComputer
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch::FindComputer


## -description


Displays the <b>Search Results: Computers</b> dialog box. The dialog box shows the result of the search for a specified computer.


## -parameters






## -returns



<h3>JScript</h3>
This method does not return a value.

<h3>VB</h3>
This method does not return a value.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/0304b955-afde-4de4-824a-9ec9c9530360">Shell.FindComputer</a> method.


#### Examples

The following examples show the use of <b>FindComputer</b> in JScript, VBScript, and Visual Basic.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FindComputer();
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
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.FindComputer

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
<pre>Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FindComputer

    Set objShell = Nothing
End Sub
</pre>
</td>
</tr>
</table></span></div>


