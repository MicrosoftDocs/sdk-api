---
UID: NF:shldisp.IShellDispatch.NameSpace
title: IShellDispatch::NameSpace
author: windows-sdk-content
description: Creates and returns a Folder object for the specified folder.
old-location: shell\IShellDispatch_NameSpace.htm
old-project: shell
ms.assetid: CEA73705-1C27-4138-86C4-1715016E2ED8
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IShellDispatch object [Windows Shell],NameSpace method, IShellDispatch.NameSpace, IShellDispatch::NameSpace, NameSpace, NameSpace method [Windows Shell], NameSpace method [Windows Shell],IShellDispatch object, shell.IShellDispatch_NameSpace
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
 - IShellDispatch.NameSpace
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch::NameSpace


## -description


Creates and returns a <a href="https://msdn.microsoft.com/f1e82c61-205e-47c8-bc7c-6a52410a672e">Folder</a> object for the specified folder.


## -parameters




### -param vDir [in]

Type: <b>Variant</b>

The folder for which to create the <a href="https://msdn.microsoft.com/f1e82c61-205e-47c8-bc7c-6a52410a672e">Folder</a> object. This can be a string that specifies the path of the folder or one of the <a href="https://msdn.microsoft.com/35338102-f3a9-4bcf-ad62-d395462e6d2c">ShellSpecialFolderConstants</a> values. Note that the constant names found in <b>ShellSpecialFolderConstants</b> are available in Visual Basic, but not in VBScript or JScript. In those cases, the numeric values must be used in their place.


### -param ppsdf






## -returns



<h3>JScript</h3>
Type: <b><a href="https://msdn.microsoft.com/f1e82c61-205e-47c8-bc7c-6a52410a672e">Folder</a>**</b>

Object reference to the <a href="https://msdn.microsoft.com/f1e82c61-205e-47c8-bc7c-6a52410a672e">Folder</a> object for the specified folder. If the folder is not successfully created, this value returns <b>null</b>.

<h3>VB</h3>
Type: <b><a href="https://msdn.microsoft.com/f1e82c61-205e-47c8-bc7c-6a52410a672e">Folder</a>**</b>

Object reference to the <a href="https://msdn.microsoft.com/f1e82c61-205e-47c8-bc7c-6a52410a672e">Folder</a> object for the specified folder. If the folder is not successfully created, this value returns <b>null</b>.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/c0d61bc6-6851-4b47-a62d-4c24d2958b98">Shell.NameSpace</a> method.


#### Examples

The following examples show the use of <a href="https://msdn.microsoft.com/c0d61bc6-6851-4b47-a62d-4c24d2958b98">NameSpace</a> in JScript, VBScript, and Visual Basic.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnShellNameSpaceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            alert(objFolder.Title);
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
    function fnShellNameSpaceVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\")

        if (not objFolder is nothing) then
            alert(objFolder.Title)
        end if

        set objFolder = nothing
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
<pre>Private Sub fnShellNameSpaceVB()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPERSONAL)

    If (Not objFolder Is Nothing) Then
        Debug.Print objFolder.Title
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
</pre>
</td>
</tr>
</table></span></div>


