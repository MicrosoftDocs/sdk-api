---
UID: NF:shldisp.IShellDispatch.Explore
title: IShellDispatch::Explore
author: windows-sdk-content
description: Opens a specified folder in a Windows Explorer window.
old-location: shell\IShellDispatch_Explore.htm
old-project: shell
ms.assetid: DB434D02-56B2-4e8f-9E43-BBF47C7BE377
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Explore, Explore method [Windows Shell], Explore method [Windows Shell],IShellDispatch object, IShellDispatch object [Windows Shell],Explore method, IShellDispatch.Explore, IShellDispatch::Explore, shell.IShellDispatch_Explore
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
 - IShellDispatch.Explore
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch::Explore


## -description


Opens a specified folder in a Windows Explorer window.


## -parameters




### -param vDir [in]

Type: <b>Variant</b>

The folder to be displayed. This can be a string that specifies the path of the folder or one of the <a href="https://msdn.microsoft.com/35338102-f3a9-4bcf-ad62-d395462e6d2c">ShellSpecialFolderConstants</a> values. Note that the constant names found in <b>ShellSpecialFolderConstants</b> are available in Visual Basic, but not in VBScript or JScript. In those cases, the numeric values must be used in their place.


## -returns



<h3>JScript</h3>
This method does not return a value.

<h3>VB</h3>
This method does not return a value.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/a788a3c4-f316-4fae-9294-3872eee8f46a">Shell.Explore</a> method.


#### Examples

The following examples show the use of <b>Explore</b> in JScript, VBScript, and Visual Basic.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnShellExploreJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Explore("C:\\");
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
    function fnShellExploreVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.Explore(ssfWINDOWS)

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
<pre>Private Sub fnShellExploreVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.Explore (ssfPERSONAL)

    Set objShell = Nothing
End Sub
</pre>
</td>
</tr>
</table></span></div>


