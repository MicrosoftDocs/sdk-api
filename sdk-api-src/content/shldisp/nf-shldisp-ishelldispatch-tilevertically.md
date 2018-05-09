---
UID: NF:shldisp.IShellDispatch.TileVertically
title: IShellDispatch::TileVertically
author: windows-driver-content
description: Tiles all of the windows on the desktop vertically. This method has the same effect as right-clicking the taskbar and selecting Show windows side by side.
old-location: shell\IShellDispatch_TileVertically.htm
old-project: shell
ms.assetid: 63CB7E20-48E6-4cfe-B0BA-0D28A7B151BD
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: IShellDispatch object [Windows Shell],TileVertically method, IShellDispatch.TileVertically, IShellDispatch::TileVertically, TileVertically, TileVertically method [Windows Shell], TileVertically method [Windows Shell],IShellDispatch object, shell.IShellDispatch_TileVertically
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
-	IShellDispatch.TileVertically
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch::TileVertically


## -description


Tiles all of the windows on the desktop vertically. This method has the same effect as right-clicking the taskbar and selecting <b>Show windows side by side</b>.


## -parameters






## -returns



<h3>JScript</h3>
This method does not return a value.

<h3>VB</h3>
This method does not return a value.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/7d0f6dbe-b5a6-431b-954f-7ef2c62c68ea">Shell.TileVertically</a> method.


#### Examples

The following examples show the use of <b>TileVertically</b> in JScript, VBScript, and Visual Basic.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnShellTileVerticallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TileVertically();
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
    function fnShellTileVerticallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TileVertically

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
<pre>Private Sub fnShellTileVerticallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TileVertically

    Set objShell = Nothing
End Sub
</pre>
</td>
</tr>
</table></span></div>


