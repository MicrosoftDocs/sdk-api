---
UID: NF:shldisp.IShellDispatch.EjectPC
title: IShellDispatch::EjectPC
author: windows-sdk-content
description: Ejects the computer from its docking station. This is the same as clicking the Start menu and selecting Eject PC, if your computer supports this command.
old-location: shell\IShellDispatch_EjectPC.htm
old-project: shell
ms.assetid: 34448D82-187C-40aa-90B4-A4111B33048B
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EjectPC, EjectPC method [Windows Shell], EjectPC method [Windows Shell],IShellDispatch object, IShellDispatch object [Windows Shell],EjectPC method, IShellDispatch.EjectPC, IShellDispatch::EjectPC, shell.IShellDispatch_EjectPC
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
 - IShellDispatch.EjectPC
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch::EjectPC


## -description


Ejects the computer from its docking station. This is the same as clicking the <b>Start</b> menu and selecting <b>Eject PC</b>, if your computer supports this command.


## -parameters






## -returns



<h3>JScript</h3>
This method does not return a value.

<h3>VB</h3>
This method does not return a value.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/eaba3dce-8fea-453f-90c2-4a9b5cb05ecc">Shell.EjectPC</a> method.


#### Examples

The following examples show the use of <b>EjectPC</b> in JScript, VBScript, and Visual Basic.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnShellEjectPCJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.EjectPC();
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
    function fnShellEjectPCVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.EjectPC

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
<pre>Private Sub fnShellEjectPCVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.EjectPC

    Set objShell = Nothing
End Sub
</pre>
</td>
</tr>
</table></span></div>


