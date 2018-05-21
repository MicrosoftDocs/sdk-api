---
UID: NF:shldisp.IShellDispatch4.ToggleDesktop
title: IShellDispatch4::ToggleDesktop
author: windows-driver-content
description: Displays or hides the desktop.
old-location: shell\IShellDispatch4_ToggleDesktop.htm
old-project: shell
ms.assetid: 60199e18-b8da-48a6-b316-e7f07ff44b78
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IShellDispatch4 object [Windows Shell],ToggleDesktop method, IShellDispatch4.ToggleDesktop, IShellDispatch4::ToggleDesktop, ToggleDesktop, ToggleDesktop method [Windows Shell], ToggleDesktop method [Windows Shell],IShellDispatch4 object, _shell_IShellDispatch4_ToggleDesktop, shell.IShellDispatch4_ToggleDesktop
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IShellDispatch4.ToggleDesktop
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch4::ToggleDesktop


## -description


Displays or hides the desktop.


## -parameters






## -returns



<h3>JScript</h3>
This method does not return a value.

<h3>VB</h3>
This method does not return a value.




## -remarks



This method has the same effect as the <b>Show Desktop</b> button on the taskbar. It either hides all open windows to show the desktop or it hides the desktop by showing all open windows. The <b>ToggleDesktop</b> method does not display a user interface, it just invokes the toggle action.


#### Examples

The following examples show the proper use of <b>ToggleDesktop</b> for JScript, VBScript, and Visual Basic.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnIShellDispatch4ToggleDesktopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ToggleDesktop();
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
    function fnIShellDispatch4ToggleDesktopVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objShell.ToggleDesktop
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
<pre>Private Sub fnIShellDispatch4ToggleDesktopVB()
    Dim objShell As Shell
            
    Set objShell = New Shell
        objShell.ToggleDesktop
    Set objShell = Nothing
End Sub
</pre>
</td>
</tr>
</table></span></div>


