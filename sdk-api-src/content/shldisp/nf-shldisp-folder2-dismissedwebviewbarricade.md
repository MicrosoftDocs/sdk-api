---
UID: NF:shldisp.Folder2.DismissedWebViewBarricade
title: Folder2::DismissedWebViewBarricade
author: windows-sdk-content
description: Called in response to the web view barricade being dismissed by the user.
old-location: shell\Folder2_DismissedWebViewBarricade.htm
old-project: shell
ms.assetid: 170893b6-c947-45b1-b717-a93a0b083bda
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: DismissedWebViewBarricade, DismissedWebViewBarricade method [Windows Shell], DismissedWebViewBarricade method [Windows Shell],Folder2 object, Folder2 object [Windows Shell],DismissedWebViewBarricade method, Folder2.DismissedWebViewBarricade, Folder2::DismissedWebViewBarricade, _win32_Folder2_DismissedWebViewBarricade, shell.Folder2_DismissedWebViewBarricade
ms.prod: windows
ms.technology: windows-sdk
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
 - Folder2.DismissedWebViewBarricade
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# Folder2::DismissedWebViewBarricade


## -description


Called in response to the web view barricade being dismissed by the user.


## -parameters






## -returns



This method does not return a value.




## -remarks



An application calls this method after the user dismisses the web view barricade.


#### Examples

The following example uses <b>DismissedWebViewBarricade</b> to specify that the web view barricade for the C:\Windows folder has been dismissed. Proper usage is shown for JScript, VBScript, and Visual Basic.

JScript:

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnFolder2ObjectDismissedWebViewBarricadeJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder2 != null)
        {
            objFolder2.DismissedWebViewBarricade();
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
    function fnFolder2ObjectDismissedWebViewBarricadeVB()
        dim objShell
        dim objFolder2

        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder2 is nothing) then
            objFolder2.DismissedWebViewBarricade()
        end if

        set objFolder2 = nothing
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
<pre>Private Sub btnDismissedWebViewBarricade_Click()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2

    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder2 Is Nothing) Then
        objFolder2.DismissedWebViewBarricade
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f1e82c61-205e-47c8-bc7c-6a52410a672e">Folder</a>



<a href="https://msdn.microsoft.com/5b52b141-ced3-4d38-8584-7dfcfe12ab56">Folder2</a>
 

 

