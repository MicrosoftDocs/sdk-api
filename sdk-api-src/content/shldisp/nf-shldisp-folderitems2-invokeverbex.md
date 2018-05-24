---
UID: NF:shldisp.FolderItems2.InvokeVerbEx
title: FolderItems2::InvokeVerbEx
author: windows-driver-content
description: Executes a verb on a collection of FolderItem objects. This method is an extension of the InvokeVerb method, allowing additional control of the operation through a set of flags.
old-location: shell\FolderItems2_InvokeVerbEx.htm
old-project: shell
ms.assetid: 2c02985d-8877-4a02-a232-6aeb1716928c
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: FolderItems2 object [Windows Shell],InvokeVerbEx method, FolderItems2.InvokeVerbEx, FolderItems2::InvokeVerbEx, InvokeVerbEx, InvokeVerbEx method [Windows Shell], InvokeVerbEx method [Windows Shell],FolderItems2 object, _win32_FolderItems2_InvokeVerbEx, shell.FolderItems2_InvokeVerbEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
-	FolderItems2.InvokeVerbEx
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# FolderItems2::InvokeVerbEx


## -description


Executes a verb on a collection of <a href="https://msdn.microsoft.com/38c0e049-2f9f-43bc-8bf2-1b7becf16e66">FolderItem</a> objects. This method is an extension of the <a href="https://msdn.microsoft.com/569bdc88-15ef-4d08-923c-4f41e5ae5a38">InvokeVerb</a> method, allowing additional control of the operation through a set of flags.


## -parameters




### -param vVerb [in, optional]

Type: <b>Variant</b>

A <b>Variant</b> with the verb string that corresponds to the command to be executed. If no verb is specified, the default verb is executed.


### -param vArgs [in, optional]

Type: <b>Variant</b>

A <b>Variant</b> that consists of a string with one or more arguments to the command specified by <i>vVerb</i>. The format of this string depends on the particular verb.


## -remarks



A verb is a string used to specify a particular action associated with an item or collection of items.  Typically, calling a verb launches a related application. For example, calling the <b>open</b> verb on a .txt file normally opens the file with a text editor, usually Microsoft Notepad. For further discussion of verbs, see <a href="https://msdn.microsoft.com/d774c3b2-4caf-460a-ac32-0ed603491d5f">Launching Applications</a>.


#### Examples

The following example uses <b>InvokeVerbEx</b> to invoke the default verb ("open") on <b>My Computer</b>. Proper usage is shown for JScript, VBScript, and Visual Basic.

JScript:

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnFolderItems2InvokeVerbExJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder;
        var ssfDRIVES = 17;
        
        objFolder = objShell.NameSpace(ssfDRIVES);
        if (objFolder != null)
        {
            var objFolderItems2;
            
            objFolderItems2 = objFolder.Items();
            if (objFolderItems2 != null)
            {
                objFolderItems2.InvokeVerbEx();
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
    function fnFolderItems2InvokeVerbExVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfDRIVES
                
            ssfWINDOWS = 17
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems2
                        
                set objFolderItems2 = objFolder.Items()
                if (not objFolderItems2 is nothing) then
                    objFolderItems2.InvokeVerbEx
                end if
                set objFolderItems2 = nothing
            end if
            set objFolder = nothing
        end if
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
<pre>Private Sub fnFolderItems2InvokeVerbExVB()
    Dim objShell      As Shell
    Dim objFolder     As Folder2
    Dim ssfDRIVES     As Long
    
    ssfDRIVES = 17
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfDRIVES)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems2 As FolderItems
            
            Set objFolderItems2 = objFolder.Items
                If (Not objFolderItems2 Is Nothing) Then
                    objFolderItems2.InvokeVerbEx
                End If
            Set objFolderItems2 = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/0ca0efb3-6831-4561-9fd1-6d0b62704931">FolderItems2</a>



<a href="https://msdn.microsoft.com/569bdc88-15ef-4d08-923c-4f41e5ae5a38">InvokeVerb</a>
 

 

