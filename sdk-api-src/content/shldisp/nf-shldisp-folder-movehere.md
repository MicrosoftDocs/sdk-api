---
UID: NF:shldisp.Folder.MoveHere
title: Folder::MoveHere
author: windows-sdk-content
description: Moves an item or items to this folder.
old-location: shell\Folder_MoveHere.htm
old-project: shell
ms.assetid: 07723dc1-5d9d-4f32-ab18-52617b0988c4
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: Folder object [Windows Shell],MoveHere method, Folder.MoveHere, Folder::MoveHere, MoveHere, MoveHere method [Windows Shell], MoveHere method [Windows Shell],Folder object, _win32_Folder_MoveHere, shell.Folder_MoveHere
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
 - Folder.MoveHere
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# Folder::MoveHere


## -description


Moves an item or items to this folder.


## -parameters




### -param vItem [in]

Type: <b>Variant</b>

The item or items to move. This can be a string that represents a file name, a <a href="https://msdn.microsoft.com/38c0e049-2f9f-43bc-8bf2-1b7becf16e66">FolderItem</a> object, or a <a href="https://msdn.microsoft.com/b99201b3-95e8-4ddd-b338-dee8d107d0a0">FolderItems</a> object.


### -param vOptions [in, optional]

Type: <b>Variant</b>

Options for the move operation. This value can be zero or a combination of the following values. These values are based upon flags defined for use with the <b>fFlags</b> member of the C++ <a href="https://msdn.microsoft.com/590d87c2-0c75-44b9-a9b5-f7c37728512b">SHFILEOPSTRUCT</a> structure. These flags are not defined as such for Visual Basic, VBScript, or JScript, so you must define them yourself or use their numeric equivalents.



#### (4)

Do not display a progress dialog box.



#### (8)

Give the file being operated on a new name in a move, copy, or rename operation if a file with the target name already exists.



#### (16)

Respond with "Yes to All" for any dialog box that is displayed.



#### (64)

Preserve undo information, if possible.



#### (128)

Perform the operation on files only if a wildcard file name (*.*) is specified.



#### (256)

Display a progress dialog box but do not show the file names.



#### (512)

Do not confirm the creation of a new directory if the operation requires one to be created.



#### (1024)

Do not display a user interface if an error occurs.



#### (2048)


<a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 4.71.</a> Do not copy the security attributes of the file.



#### (4096)

Only operate in the local directory. Do not operate recursively into subdirectories.



#### (9182)


<a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 5.0.</a> Do not move connected files as a group. Only move the specified files.


## -returns



This method does not return a value.




## -remarks



<div class="alert"><b>Note</b>  Not all methods are implemented for all folders. For example, the <a href="https://msdn.microsoft.com/3af7052c-fb81-4a96-9bf9-379b0365a376">ParseName</a> method is not implemented for the Control Panel folder (CSIDL_CONTROLS). If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</div>
<div> </div>

#### Examples

The following example uses <b>MoveHere</b> to move the file Temp.txt from the root directory of the C drive to the C:\Windows folder. Proper usage is shown for JScript, VBScript, and Visual Basic.

JScript:

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    var FOF_NOCONFIRMATION = 16;

    function fnFolderObjectMoveHereJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.MoveHere ("C:\\temp.txt", FOF_NOCONFIRMATION);
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
    private const FOF_NOCONFIRMATION = 16
    
    function fnFolderObjectMoveHereVB()
        dim objShell
        dim objFolder

        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            objFolder.MoveHere "C:\temp.txt", FOF_NOCONFIRMATION
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
<pre>Private Const FOF_NOCONFIRMATION = &amp;H10

Private Sub btnMoveHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        objFolder.MoveHere "c:\temp.txt", FOF_NOCONFIRMATION
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
</pre>
</td>
</tr>
</table></span></div>


