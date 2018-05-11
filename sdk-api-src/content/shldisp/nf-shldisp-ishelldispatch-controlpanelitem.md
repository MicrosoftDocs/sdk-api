---
UID: NF:shldisp.IShellDispatch.ControlPanelItem
title: IShellDispatch::ControlPanelItem
author: windows-driver-content
description: Runs the specified Control Panel application.
old-location: shell\IShellDispatch_ControlPanelItem.htm
old-project: shell
ms.assetid: 9A9B6B3F-FBBC-4e76-8018-8858B6392276
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ControlPanelItem, ControlPanelItem method [Windows Shell], ControlPanelItem method [Windows Shell],IShellDispatch object, IShellDispatch object [Windows Shell],ControlPanelItem method, IShellDispatch.ControlPanelItem, IShellDispatch::ControlPanelItem, shell.IShellDispatch_ControlPanelItem
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
-	IShellDispatch.ControlPanelItem
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch::ControlPanelItem


## -description


Runs the specified Control Panel application. If the application is already open, it will activate the running instance.

            
<div class="alert"><b>Note</b>  As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function. To open those Control Panel applications, pass the canonical name to control.exe. For example:

                <pre class="syntax" xml:space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</div><div> </div>

## -parameters




### -param bstrDir [in]

Type: <b><a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a></b>

The Control Panel application's file name.


## -returns



<h3>JScript</h3>
This method does not return a value.

<h3>VB</h3>
This method does not return a value.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/54979bbd-b36b-4b5b-a8a0-5f63e9526fa5">Shell.ControlPanelItem</a> method.


#### Examples

The following examples use <a href="https://msdn.microsoft.com/54979bbd-b36b-4b5b-a8a0-5f63e9526fa5">ControlPanelItem</a> to run the Control Panel's <b>Display Properties</b> item. Usage is shown for JScript, VBScript, and Visual Basic.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>
&lt;script language="JScript"&gt;
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Shell_ControlPanelItem("desk.cpl");
    }
&lt;/script&gt;</pre>
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
<pre>
&lt;script language="VBScript"&gt;
    function fnShellControlPanelItemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Shell_ControlPanelItem("desk.cpl")
       
        set objShell = nothing
    end function
 &lt;/script&gt;</pre>
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
<pre>
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Shell_ControlPanelItem ("desk.cpl")
    
    Set objShell = Nothing
End Sub</pre>
</td>
</tr>
</table></span></div>


