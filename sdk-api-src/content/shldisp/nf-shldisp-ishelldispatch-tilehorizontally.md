---
UID: NF:shldisp.IShellDispatch.TileHorizontally
title: IShellDispatch::TileHorizontally
author: windows-driver-content
description: Tiles all of the windows on the desktop horizontally. This method has the same effect as right-clicking the taskbar and selecting Show windows stacked.
old-location: shell\IShellDispatch_TileHorizontally.htm
old-project: shell
ms.assetid: 85785510-6B75-450a-A9BB-6C3B4F6194E2
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: IShellDispatch object [Windows Shell],TileHorizontally method, IShellDispatch.TileHorizontally, IShellDispatch::TileHorizontally, TileHorizontally, TileHorizontally method [Windows Shell], TileHorizontally method [Windows Shell],IShellDispatch object, shell.IShellDispatch_TileHorizontally
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
-	IShellDispatch.TileHorizontally
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch::TileHorizontally


## -description


Tiles all of the windows on the desktop horizontally. This method has the same effect as right-clicking the taskbar and selecting <b>Show windows stacked</b>.


## -parameters






## -returns



<h3>JScript</h3>
This method does not return a value.

<h3>VB</h3>
This method does not return a value.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/b0e06766-1bd4-4744-81f3-139b018aa72c">Shell.TileHorizontally</a> method.


#### Examples

The following example shows the use of <b>TileHorizontally</b> in JScript, VBScript, and Visual Basic.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnShellTileHorizontallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TileHorizontally();
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
    function fnShellTileHorizontallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TileHorizontally

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
<pre>Private Sub fnShellTileHorizontallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TileHorizontally

    Set objShell = Nothing
End Sub
</pre>
</td>
</tr>
</table></span></div>


