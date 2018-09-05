---
UID: NF:shldisp.IShellDispatch4.WindowsSecurity
title: IShellDispatch4::WindowsSecurity
author: windows-sdk-content
description: Displays the Windows Security dialog box.
old-location: shell\IShellDispatch4_WindowsSecurity.htm
old-project: shell
ms.assetid: 665c4644-7749-446e-8212-3ecc9901a035
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IShellDispatch4 object [Windows Shell],WindowsSecurity method, IShellDispatch4.WindowsSecurity, IShellDispatch4::WindowsSecurity, WindowsSecurity, WindowsSecurity method [Windows Shell], WindowsSecurity method [Windows Shell],IShellDispatch4 object, _shell_IShellDispatch4_WindowsSecurity, shell.IShellDispatch4_WindowsSecurity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shldisp.h
req.include-header: 
req.redist: 
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
 - IShellDispatch4.WindowsSecurity
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch4::WindowsSecurity


## -description


Displays the <b>Windows Security</b> dialog box.


## -parameters






## -returns



<h3>JScript</h3>
This method does not return a value.

<h3>VB</h3>
This method does not return a value.




## -remarks



This method displays the dialog box shown after pressing CTRL+ALT+DELETE or using the security option on the <b>Start</b> menu.



<div class="alert"><b>Note</b>  This method can be used only when connected by a terminal session to Microsoft Terminal Server.</div>
<div> </div>

#### Examples

The following examples show the use of <b>WindowsSecurity</b> for JScript, VBScript, and Visual Basic.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
     function fnIShellDispatch4WindowsSecurityJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.WindowsSecurity();
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
     function fnIShellDispatch4WindowsSecurityVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objshell.WindowsSecurity
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
<pre>Private Sub fnIShellDispatch4WindowsSecurityVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        objshell.WindowsSecurity
    Set objShell = Nothing
End Sub
</pre>
</td>
</tr>
</table></span></div>


