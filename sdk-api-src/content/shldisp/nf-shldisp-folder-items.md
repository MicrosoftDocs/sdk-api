---
UID: NF:shldisp.Folder.Items
title: Folder::Items
author: windows-driver-content
description: Retrieves a FolderItems object that represents the collection of items in the folder.
old-location: shell\Folder_Items.htm
old-project: shell
ms.assetid: ef2965ec-c8ab-4108-8e5e-b4fd5370521a
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: Folder object [Windows Shell],Items method, Folder.Items, Folder::Items, Items, Items method [Windows Shell], Items method [Windows Shell],Folder object, _win32_Folder_Items, shell.Folder_Items
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
-	Folder.Items
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# Folder::Items


## -description


Retrieves a <a href="https://msdn.microsoft.com/b99201b3-95e8-4ddd-b338-dee8d107d0a0">FolderItems</a> object that represents the collection of items in the folder.


## -parameters




### -param ppid






## -returns



Type: <b><a href="https://msdn.microsoft.com/b99201b3-95e8-4ddd-b338-dee8d107d0a0">FolderItems</a>**</b>

An object reference to the <a href="https://msdn.microsoft.com/b99201b3-95e8-4ddd-b338-dee8d107d0a0">FolderItems</a> object.




## -remarks



<div class="alert"><b>Note</b>  Not all methods are implemented for all folders. For example, the <a href="https://msdn.microsoft.com/3af7052c-fb81-4a96-9bf9-379b0365a376">ParseName</a> method is not implemented for the Control Panel folder (CSIDL_CONTROLS). If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</div>
<div> </div>

#### Examples

The following example uses <b>Items</b> to determine the number of items in the C:\Windows folder. Proper usage is shown for JScript, VBScript, and Visual Basic.

JScript:

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnFolderObjectItemsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItems = new Object;
            
            objFolderItems = objFolder.Items();
            if (objFolderItems != null)
            {
                document.write (objFolderItems.Count);
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
    function fnFolderObjectItemsVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItems

            set objFolderItems = objFolder.Items

            if (not objFolderItems Is Nothing) then
                document.write objFolderItems.Count
            end if

            set objFolderItem = nothing
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
<pre>Private Sub btnFolderObjectItems_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        Dim objFolderItems As FolderItems

        Set objFolderItems = objFolder.Items()

        If (Not objFolderItems Is Nothing) Then
            Dim vCount As Variant

            vCount = objFolderItems.Count
        End If

        Set objFolderItems = Nothing
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
</pre>
</td>
</tr>
</table></span></div>


