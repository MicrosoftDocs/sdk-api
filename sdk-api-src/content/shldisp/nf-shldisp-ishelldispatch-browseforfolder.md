---
UID: NF:shldisp.IShellDispatch.BrowseForFolder
title: IShellDispatch::BrowseForFolder
author: windows-sdk-content
description: Creates a dialog box that enables the user to select a folder and then returns the selected folder's Folder object.
old-location: shell\IShellDispatch_BrowseForFolder.htm
old-project: shell
ms.assetid: 578C51C1-F59B-4604-A09B-62BA61225ABB
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: BrowseForFolder, BrowseForFolder method [Windows Shell], BrowseForFolder method [Windows Shell],IShellDispatch object, IShellDispatch object [Windows Shell],BrowseForFolder method, IShellDispatch.BrowseForFolder, IShellDispatch::BrowseForFolder, shell.IShellDispatch_BrowseForFolder
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
 - IShellDispatch.BrowseForFolder
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch::BrowseForFolder


## -description


Creates a dialog box that enables the user to select a folder and then returns the selected folder's <a href="https://msdn.microsoft.com/f1e82c61-205e-47c8-bc7c-6a52410a672e">Folder</a> object.


## -parameters




### -param Hwnd [in]

Type: <b>Integer</b>

The handle to the parent window of the dialog box. This value can be zero.


### -param Title




### -param Options




### -param RootFolder




### -param ppsdf






#### - iOptions [in]

Type: <b>Integer</b>

An <b>Integer</b> value that contains the options for the method. This can be zero or a combination of the values listed under the <b>ulFlags</b> member of the <a href="https://msdn.microsoft.com/7c8df03a-93bb-42b2-b4a0-9c2ae917c0d1">BROWSEINFO</a> structure.


#### - sTitle [in]

Type: <b><a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a></b>

A <b>String</b> value that represents the title displayed inside the <b>Browse</b> dialog box.


#### - vRootFolder [in, optional]

Type: <b>Variant</b>

The root folder to use in the dialog box. The user cannot browse higher in the tree than this folder. If this value is not specified, the root folder used in the dialog box is the desktop. This value can be a string that specifies the path of the folder or one of the <a href="https://msdn.microsoft.com/35338102-f3a9-4bcf-ad62-d395462e6d2c">ShellSpecialFolderConstants</a> values. Note that the constant names found in <b>ShellSpecialFolderConstants</b> are available in Visual Basic, but not in VBScript or JScript. In those cases, the numeric values must be used in their place.


## -returns



<h3>JScript</h3>
Type: <b>FOLDER**</b>

An object reference to the selected folder's <a href="https://msdn.microsoft.com/f1e82c61-205e-47c8-bc7c-6a52410a672e">Folder</a> object.

<h3>VB</h3>
Type: <b>FOLDER**</b>

An object reference to the selected folder's <a href="https://msdn.microsoft.com/f1e82c61-205e-47c8-bc7c-6a52410a672e">Folder</a> object.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/4cc44e5a-3578-448b-9b19-1b71e1ae2cb9">Shell.BrowseForFolder</a> method.


#### Examples

The following examples use <b>BrowseForFolder</b> to display a browse window titled "Example" rooted at the Windows folder. Usage is shown for JScript, VBScript, and Visual Basic.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnShellBrowseForFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS);
        if (objFolder != null)
        {
            // Add code here.
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
    function fnShellBrowseForFolderVB()
        dim objShell
        dim ssfWINDOWS
        dim objFolder
        
        ssfWINDOWS = 36
        set objShell = CreateObject("shell.application")
            set objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
                if (not objFolder is nothing) then
                    'Add code here.
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
<pre>Private Sub fnShellBrowseForFolderVB()
    Dim objShell   As Shell
    Dim ssfWINDOWS As Long
    Dim objFolder  As Folder
    
    ssfWINDOWS = 36
    Set objShell = New Shell
        Set objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
            If (Not objFolder Is Nothing) Then
                'Add code here
            End If
        Set objFolder = Nothing
    Set objShell = Nothing
End Sub
</pre>
</td>
</tr>
</table></span></div>


