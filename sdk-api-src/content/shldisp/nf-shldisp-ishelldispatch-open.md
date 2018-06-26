---
UID: NF:shldisp.IShellDispatch.Open
title: IShellDispatch::Open
author: windows-sdk-content
description: Opens the specified folder.
old-location: shell\IShellDispatch_Open.htm
old-project: shell
ms.assetid: 30FE669A-4AFD-4dfa-9F62-E62E744469C7
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: IShellDispatch object [Windows Shell],Open method, IShellDispatch.Open, IShellDispatch::Open, Open, Open method [Windows Shell], Open method [Windows Shell],IShellDispatch object, shell.IShellDispatch_Open
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
 - IShellDispatch.Open
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch::Open


## -description


Opens the specified folder.


## -parameters




### -param vDir [in]

Type: <b>Variant</b>

A string that specifies the path of the folder or one of the <a href="https://msdn.microsoft.com/35338102-f3a9-4bcf-ad62-d395462e6d2c">ShellSpecialFolderConstants</a> values.  Note that the constant names found in <b>ShellSpecialFolderConstants</b> are available in Visual Basic, but not in VBScript or JScript. In those cases, the numeric values must be used in their place.

If <i>vDir</i> is set to one of the <a href="https://msdn.microsoft.com/35338102-f3a9-4bcf-ad62-d395462e6d2c">ShellSpecialFolderConstants</a> and the special folder does not exist, this function will create the folder.


## -returns



<h3>JScript</h3>
This method does not return a value.

<h3>VB</h3>
This method does not return a value.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/96ed9360-fb8f-4f7e-aefb-4a63ec95df07">Shell.Open</a> method.


#### Examples

The following examples show the use of <b>Open</b> in JScript, VBScript, and Visual Basic.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnShellOpenJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36
        
        objshell.Open(ssfWINDOWS);
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
    function fnShellOpenVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Open("C:\")

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
<pre>Private Sub fnShellOpenVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Open (ssfPERSONAL)

    Set objShell = Nothing
End Sub
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/a788a3c4-f316-4fae-9294-3872eee8f46a">Explore</a>



<a href="https://msdn.microsoft.com/9B429C03-7F80-45db-B8CD-58D19FAD2E61">IShellDispatch</a>
 

 

