---
UID: NF:shldisp.IShellDispatch.ShutdownWindows
title: IShellDispatch::ShutdownWindows
author: windows-sdk-content
description: Displays the Shut Down Windows dialog box. This is the same as clicking the Start menu and selecting Shut Down.
old-location: shell\IShellDispatch_ShutdownWindows.htm
old-project: shell
ms.assetid: 3C4F6579-6398-4af4-8911-FE22555B0ABC
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IShellDispatch object [Windows Shell],ShutdownWindows method, IShellDispatch.ShutdownWindows, IShellDispatch::ShutdownWindows, ShutdownWindows, ShutdownWindows method [Windows Shell], ShutdownWindows method [Windows Shell],IShellDispatch object, shell.IShellDispatch_ShutdownWindows
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shldisp.h
req.include-header: 
req.redist: 
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
 - IShellDispatch.ShutdownWindows
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch::ShutdownWindows


## -description


Displays the <b>Shut Down Windows</b> dialog box. This is the same as clicking the <b>Start</b> menu and selecting <b>Shut Down</b>.


## -parameters






## -returns



<h3>JScript</h3>
This method does not return a value.

<h3>VB</h3>
This method does not return a value.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/6fa8e2e0-a58f-4837-89f5-898cece2d80a">Shell.ShutdownWindows</a> method.


#### Examples

The following example shows the use of <b>ShutdownWindows</b> in JScript, VBScript, and Visual Basic.

JScript:
                


```javascript
<script language="JScript">
    function fnShellShutdownWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.ShutdownWindows();
    }
</script>

```


VBScript:


```vb
<script language="VBScript">
    function fnShellShutdownWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.ShutdownWindows

        set objShell = nothing
    end function
 </script>

```


Visual Basic:


```vb
Private Sub fnShellShutdownWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.ShutdownWindows

    Set objShell = Nothing
End Sub

```




