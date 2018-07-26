---
UID: NF:shldisp.IShellDispatch.RefreshMenu
title: IShellDispatch::RefreshMenu
author: windows-sdk-content
description: Refreshes the contents of the Start menu. Used only with systems preceding Windows XP.
old-location: shell\IShellDispatch_RefreshMenu.htm
old-project: shell
ms.assetid: D36FA5A0-AF03-4627-86E0-869BF1440958
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IShellDispatch object [Windows Shell],RefreshMenu method, IShellDispatch.RefreshMenu, IShellDispatch::RefreshMenu, RefreshMenu, RefreshMenu method [Windows Shell], RefreshMenu method [Windows Shell],IShellDispatch object, shell.IShellDispatch_RefreshMenu
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
 - IShellDispatch.RefreshMenu
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch::RefreshMenu


## -description


Refreshes the contents of the <b>Start</b> menu. Used only with systems preceding Windows XP.


## -parameters






## -returns



<h3>JScript</h3>
This method does not return a value.

<h3>VB</h3>
This method does not return a value.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/0d82d847-9e6f-461e-b938-fe8fd49a636f">Shell.TrayProperties</a> method.

The functionality that <b>RefreshMenu</b> provides is handled automatically under Windows XP or later. Do not call this method on Windows XP or later.


#### Examples

The following examples show the use of <b>RefreshMenu</b> in JScript, VBScript, and Visual Basic.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.RefreshMenu();
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
    function fnShellRefreshMenuVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.RefreshMenu

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
<pre>Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.RefreshMenu

    Set objShell = Nothing
End Sub
</pre>
</td>
</tr>
</table></span></div>


