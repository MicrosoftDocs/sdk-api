---
UID: NF:shldisp.IShellDispatch2.ShellExecute
title: IShellDispatch2::ShellExecute
author: windows-sdk-content
description: Performs a specified operation on a specified file.
old-location: shell\IShellDispatch2_ShellExecute.htm
old-project: shell
ms.assetid: a55e804c-ed7c-4b22-b86f-8e5653976654
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: IShellDispatch2 object [Windows Shell],ShellExecute method, IShellDispatch2.ShellExecute, IShellDispatch2::ShellExecute, ShellExecute, ShellExecute method [Windows Shell], ShellExecute method [Windows Shell],IShellDispatch2 object, _win32_IShellDispatch2_ShellExecute, shell.IShellDispatch2_ShellExecute
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IShellDispatch2.ShellExecute
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch2::ShellExecute


## -description


Performs a specified operation on a specified file.


## -parameters




### -param File




### -param vArgs




### -param vDir




### -param vOperation [in, optional]

Type: <b>Variant</b>

The operation to be performed. This value is set to one of the verb strings that is supported by the file. For a discussion of verbs, see the Remarks section. If this parameter is not specified, the default operation is performed.


### -param vShow [in, optional]

Type: <b>Variant</b>

A recommendation as to how the application window should be displayed initially. The application can ignore this recommendation. This parameter can be one of the following values. If this parameter is not specified, the application uses its default value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Open the application with a hidden window.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Open the application with a normal window. If the window is minimized or maximized, the system restores it to its original size and position.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Open the application with a minimized window.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Open the application with a maximized window.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Open the application with its window at its most recent size and position. The active window remains active.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Open the application with its window at its current size and position.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
Open the application with a minimized window. The active window remains active.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
Open the application with its window in the default state specified by the application.

</td>
</tr>
</table>
 


#### - sFile [in]

Type: <b><a href="https://msdn.microsoft.com/library/ms221069(v=VS.85).aspx">BSTR</a></b>

A <b>String</b> that contains the name of the file on which <b>ShellExecute</b> will perform the action specified by <i>vOperation</i>.


#### - vArguments [in, optional]

Type: <b>Variant</b>

A string that contains parameter values for the operation.


#### - vDirectory [in, optional]

Type: <b>Variant</b>

The fully qualified path of the directory that contains the file specified by <i>sFile</i>. If this parameter is not specified, the current working directory is used.


## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/62E59A1C-51BD-4864-AF09-35FFD49FAB9D">Shell.ShellExecute</a> method.

This method is equivalent to launching one of the commands associated with a file's shortcut menu. Each command is represented by a verb string. The set of supported verbs varies from file to file. The most commonly supported verb is "open", which is also usually the default verb. Other verbs might be supported by only certain types of files. For further discussion of Shell verbs, see <a href="https://msdn.microsoft.com/d774c3b2-4caf-460a-ac32-0ed603491d5f">Launching Applications</a> or <a href="https://msdn.microsoft.com/d951d1e8-0f88-49c4-8373-e6db0e18cd72">Extending Shortcut Menus</a>.

This method is not currently available in Microsoft Visual Basic.


#### Examples

The following examples show the use of <b>ShellExecute</b> to open Notepad. Usage is shown for JScript and VBScript.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnShellExecuteJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShellExecute("notepad.exe", "", "", "open", 1);
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
    function fnShellExecuteVB()
        dim objShell

        set objShell = CreateObject("shell.application")

        objShell.ShellExecute "notepad.exe", "", "", "open", 1

        set objShell = nothing
    end function
&lt;/script&gt;
</pre>
</td>
</tr>
</table></span></div>


