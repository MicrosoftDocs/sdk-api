---
UID: NF:shldisp.Folder.GetDetailsOf
title: Folder::GetDetailsOf
author: windows-driver-content
description: Retrieves details about an item in a folder. For example, its size, type, or the time of its last modification.
old-location: shell\Folder_GetDetailsOf.htm
old-project: shell
ms.assetid: d2fe4550-f171-40d9-8bce-065b61826997
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: Folder object [Windows Shell],GetDetailsOf method, Folder.GetDetailsOf, Folder::GetDetailsOf, GetDetailsOf, GetDetailsOf method [Windows Shell], GetDetailsOf method [Windows Shell],Folder object, _win32_Folder_GetDetailsOf, shell.Folder_GetDetailsOf
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shldisp.h
req.include-header: Shldisp.h
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
-	Folder.GetDetailsOf
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# Folder::GetDetailsOf


## -description


Retrieves details about an item in a folder. For example, its size, type, or the time of its last modification.


## -parameters




### -param vItem

Type: <b>Variant</b>

The item for which to retrieve the information. This must be a <a href="https://msdn.microsoft.com/38c0e049-2f9f-43bc-8bf2-1b7becf16e66">FolderItem</a> object.


### -param iColumn

Type: <b>Integer</b>

An <b>Integer</b> value that specifies the information to be retrieved. The information available for an item depends on the folder in which it is displayed. This value corresponds to the zero-based column number that is displayed in a Shell view. For an item in the file system, this can be one of the following values:



#### (0)

Retrieves the name of the item.



#### (1)

Retrieves the size of the item.



#### (2)

Retrieves the type of the item.



#### (3)

Retrieves the date and time that the item was last modified.



#### (4)

Retrieves the attributes of the item.



#### (-1)

Retrieves the info tip information for the item.


### -param pbs






## -returns



Type: <b><a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a>*</b>

String containing the retrieved detail.




## -remarks



<div class="alert"><b>Note</b>  Not all methods are implemented for all folders. For example, the <a href="https://msdn.microsoft.com/3af7052c-fb81-4a96-9bf9-379b0365a376">ParseName</a> method is not implemented for the Control Panel folder (CSIDL_CONTROLS). If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</div>
<div> </div>

#### Examples

The following example uses <b>GetDetailsOf</b> to retrieve the type of the file named Clock.avi. Proper usage is shown for JScript, VBScript, and Visual Basic.

JScript:

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnGetDetailsOfJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItem = new Object;

            objFolderItem = objFolder.ParseName("clock.avi");
            if (objFolderItem != null)
            {
                var objInfo = new Object;

                objInfo = objFolder.GetDetailsOf(objFolderItem, 2);
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
    function fnGetDetailsOfVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItem

            set objFolderItem = objFolder.ParseName("clock.avi")

            if (not objFolderItem Is Nothing) then
                dim objInfo
                        
                objInfo = objFolder.GetDetailsOf(objFolderItem, 2)
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
<pre>Private Sub btnGetDetailsOf_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
    
    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
        Set objFolderItem = objFolder.ParseName("clock.avi")
   
        If (Not objFolderItem Is Nothing) Then
            Dim szItem As String
            szItem = objFolder.GetDetailsOf(objFolderItem, 2)
        End If
        
        Set objFolderItem = Nothing
    End If
    
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
</pre>
</td>
</tr>
</table></span></div>


