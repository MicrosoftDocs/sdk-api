---
UID: NF:shldisp.FolderItem.InvokeVerb
title: FolderItem::InvokeVerb
author: windows-driver-content
description: Executes a verb on the item.
old-location: shell\FolderItem_InvokeVerb.htm
old-project: shell
ms.assetid: 569bdc88-15ef-4d08-923c-4f41e5ae5a38
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: FolderItem object [Windows Shell],InvokeVerb method, FolderItem.InvokeVerb, FolderItem::InvokeVerb, InvokeVerb, InvokeVerb method [Windows Shell], InvokeVerb method [Windows Shell],FolderItem object, _win32_FolderItem_InvokeVerb, shell.FolderItem_InvokeVerb
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
-	FolderItem.InvokeVerb
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# FolderItem::InvokeVerb


## -description


Executes a verb on the item.


## -parameters




### -param vVerb [in, optional]

Type: <b>Variant</b>

A string that specifies the verb to be executed. It must be one of the values returned by the item's <a href="https://msdn.microsoft.com/d18fddac-eb51-4031-a572-1bfef2f757a9">FolderItemVerb.Name</a> property. If no verb is specified, the default verb will be invoked.


## -returns



This method does not return a value.




## -remarks



A verb is a string used to specify a particular action that an item supports. Invoking a verb is equivalent to selecting a command from an item's shortcut menu. Typically, invoking a verb launches a related application. For example, invoking the "open" verb on a .txt file opens the file with a text editor, usually Microsoft Notepad. See <a href="https://msdn.microsoft.com/d774c3b2-4caf-460a-ac32-0ed603491d5f">Launching Applications</a> for further discussion of verbs.

The <a href="https://msdn.microsoft.com/31badb4b-b89e-4294-9dd7-bda716e163b2">FolderItemVerbs</a> object represents the collection of verbs associated with the item. The default verb may vary for different items, but it is typically "open".


#### Examples

The following example uses <b>InvokeVerb</b> to invoke the default verb ("open" in this case) on the Windows folder. Proper usage is shown for JScript, VBScript, and Visual Basic.

JScript:

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnFolderItemInvokeVerbJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                var szReturn;
                
                objFolderItem.InvokeVerb();
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
    function fnFolderItemInvokeVerbVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    dim szReturn
                                
                    objFolderItem.InvokeVerb()
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
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
<pre>Private Sub fnFolderItemInvokeVerbVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.Self
                If (Not objFolderItem Is Nothing) Then
                    Dim szReturn As String
                    
                    objFolderItem.InvokeVerb
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/92400fe9-e4d1-4bc9-b4ee-d2adaf38154f">DoIt</a>



<a href="https://msdn.microsoft.com/38c0e049-2f9f-43bc-8bf2-1b7becf16e66">FolderItem</a>



<a href="https://msdn.microsoft.com/e31160cd-093a-45a6-a066-58120c44eb2c">Verbs</a>
 

 

