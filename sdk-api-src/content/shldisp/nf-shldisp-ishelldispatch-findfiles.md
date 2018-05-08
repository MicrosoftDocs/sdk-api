---
UID: NF:shldisp.IShellDispatch.FindFiles
title: IShellDispatch::FindFiles
author: windows-driver-content
description: Displays the Find:\_All Files dialog box. This is the same as clicking the Start menu and then selecting Search.
old-location: shell\IShellDispatch_FindFiles.htm
old-project: shell
ms.assetid: 6F588D5E-5B6E-4000-BAD5-B557FB975FCA
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: FindFiles, FindFiles method [Windows Shell], FindFiles method [Windows Shell],IShellDispatch object, IShellDispatch object [Windows Shell],FindFiles method, IShellDispatch.FindFiles, IShellDispatch::FindFiles, shell.IShellDispatch_FindFiles
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IShellDispatch.FindFiles
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch::FindFiles


## -description


Displays the <b>Find: All Files</b> dialog box. This is the same as clicking the <b>Start</b> menu and then selecting <b>Search</b>.


## -parameters






## -returns



<h3>JScript</h3>
This method does not return a value.

<h3>VB</h3>
This method does not return a value.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/cccdd3ea-b52a-4fbe-b4c5-1efc1dd6d770">Shell.FindFiles</a> method.


#### Examples

The following examples show the use of <b>FindFiles</b> in JScript, VBScript, and Visual Basic.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnShellFindFilesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindFiles();
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
   function fnShellFindFilesVB()
       dim objShell
       
       set objShell = CreateObject("shell.application")
       objshell.FindFiles

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
<pre>Private Sub fnShellFindFilesVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindFiles

    Set objShell = Nothing
End Sub
</pre>
</td>
</tr>
</table></span></div>


