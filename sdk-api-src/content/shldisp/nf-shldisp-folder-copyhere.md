---
UID: NF:shldisp.Folder.CopyHere
title: Folder::CopyHere
author: windows-sdk-content
description: Copies an item or items to a folder.
old-location: shell\Folder_CopyHere.htm
old-project: shell
ms.assetid: 22bf1b4c-f242-4c52-b094-c5339bb35d02
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: CopyHere, CopyHere method [Windows Shell], CopyHere method [Windows Shell],Folder object, Folder object [Windows Shell],CopyHere method, Folder.CopyHere, Folder::CopyHere, _win32_Folder_CopyHere, shell.Folder_CopyHere
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
 - Folder.CopyHere
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# Folder::CopyHere


## -description


Copies an item or items to a folder.


## -parameters




### -param vItem

Type: <b>Variant</b>

The item or items to copy. This can be a string that represents a file name, a <a href="https://msdn.microsoft.com/38c0e049-2f9f-43bc-8bf2-1b7becf16e66">FolderItem</a> object, or a <a href="https://msdn.microsoft.com/b99201b3-95e8-4ddd-b338-dee8d107d0a0">FolderItems</a> object.


### -param vOptions [optional]

Type: <b>Variant</b>

Options for the copy operation. This value can be zero or a combination of the following values. These values are based upon flags defined for use with the <b>fFlags</b> member of the C++ <a href="https://msdn.microsoft.com/590d87c2-0c75-44b9-a9b5-f7c37728512b">SHFILEOPSTRUCT</a> structure. Each Shell namespace must provide its own implementation of these flags, and each namespace can choose to ignore some or even all of these flags. These flags are not defined by name for Visual Basic, VBScript, or JScript, so you must define them yourself or use their numeric equivalents.

                        

<div class="alert"><b>Note</b>  In some cases, such as compressed (.zip) files, some option flags may be ignored by design.</div>
<div> </div>


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



#### (8192)


<a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 5.0.</a> Do not copy connected files as a group. Only copy the specified files.


## -returns



This method does not return a value.




## -remarks



No notification is given to the calling program to indicate that the copy has completed.

<div class="alert"><b>Note</b>  Not all methods are implemented for all folders. For example, the <a href="https://msdn.microsoft.com/3af7052c-fb81-4a96-9bf9-379b0365a376">ParseName</a> method is not implemented for the Control Panel folder (CSIDL_CONTROLS). If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</div>
<div> </div>

#### Examples

The following example uses <b>CopyHere</b> to copy the Autoexec.bat file from the root directory to the C:\Windows directory. Proper usage is shown for JScript, VBScript, and Visual Basic.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnCopyHereJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.CopyHere("C:\\AUTOEXEC.BAT");
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
    function fnCopyHereVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")
 
        if not objFolder is nothing then
            objFolder.CopyHere("C:\AUTOEXEC.BAT")
        end if
 
        set objShell = nothing
        set objFolder = nothing
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
<pre>Private Sub btnCopyHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
 
    If (Not objFolder Is Nothing) Then
        objFolder.CopyHere ("C:\AUTOEXEC.BAT")
    End If
 
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f1e82c61-205e-47c8-bc7c-6a52410a672e">Folder</a>
 

 

