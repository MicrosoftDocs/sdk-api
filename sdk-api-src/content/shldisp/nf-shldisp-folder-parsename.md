---
UID: NF:shldisp.Folder.ParseName
title: Folder::ParseName
author: windows-sdk-content
description: Creates and returns a FolderItem object that represents a specified item.
old-location: shell\Folder_ParseName.htm
old-project: shell
ms.assetid: 3af7052c-fb81-4a96-9bf9-379b0365a376
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: Folder object [Windows Shell],ParseName method, Folder.ParseName, Folder::ParseName, ParseName, ParseName method [Windows Shell], ParseName method [Windows Shell],Folder object, _win32_Folder_ParseName, shell.Folder_ParseName
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
 - Folder.ParseName
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# Folder::ParseName


## -description


Creates and returns a <a href="https://msdn.microsoft.com/38c0e049-2f9f-43bc-8bf2-1b7becf16e66">FolderItem</a> object that represents a specified item.


## -parameters




### -param bName [in]

Type: <b><a href="https://msdn.microsoft.com/library/ms221069(v=VS.85).aspx">BSTR</a></b>

A string that specifies the name of the item.


### -param ppid






## -returns



Type: <b><a href="https://msdn.microsoft.com/38c0e049-2f9f-43bc-8bf2-1b7becf16e66">FolderItem</a>**</b>

An object reference to the <a href="https://msdn.microsoft.com/38c0e049-2f9f-43bc-8bf2-1b7becf16e66">FolderItem</a> object.




## -remarks



<b>ParseName</b> should not be used for virtual folders such as My Documents.


#### Examples

The following example uses <b>ParseName</b> to create an object representing the folder item Clock.avi in the C:\Windows folder. Proper usage is shown for JScript, VBScript, and Visual Basic.

JScript:

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnFolderObjectParseNameJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItem = new Object;
            
            objFolderItem = objFolder.ParseName("clock.avi");
            if (objFolderItem != null)
            {
                //Add code here.
            }
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
    function fnFolderObjectParseNameVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItem
            
            set objFolderItem = objFolder.ParseName("clock.avi")

            if (not objFolderItem is nothing) then
                'Add code here.
            end if
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
<pre>Private Sub btnParseName_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
        
        Set objFolderItem = objFolder.ParseName("clock.avi")
            'Add code here.
            Debug.Print "passed"
        Set objFolderItem = Nothing
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
</pre>
</td>
</tr>
</table></span></div>


