---
UID: NF:shldisp.IShellDispatch.FileRun
title: IShellDispatch::FileRun
author: windows-sdk-content
description: Displays the Run dialog to the user.
old-location: shell\IShellDispatch_FileRun.htm
old-project: shell
ms.assetid: BC7C4C26-593D-4467-A2AA-4F2DF835C989
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FileRun, FileRun method [Windows Shell], FileRun method [Windows Shell],IShellDispatch object, IShellDispatch object [Windows Shell],FileRun method, IShellDispatch.FileRun, IShellDispatch::FileRun, shell.IShellDispatch_FileRun
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
 - IShellDispatch.FileRun
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch::FileRun


## -description


Displays the <b>Run</b> dialog to the user.


## -parameters






## -returns



<h3>JScript</h3>
This method does not return a value.

<h3>VB</h3>
This method does not return a value.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/bb984777-e09f-41e6-8359-51c5291654f7">Shell.FileRun</a> method.


#### Examples

The following examples show the use of <b>FileRun</b> in JScript, VBScript, and Visual Basic.

JScript:
                


```javascript
<script language="JScript">
    function fnShellFileRunJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FileRun();
    }
</script>

```


VBScript:


```vb
<script language="VBScript">
    function fnShellFileRunVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.FileRun

        set objShell = nothing
    end function
 </script>

```


Visual Basic:


```vb
Private Sub fnShellFileRunVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FileRun

    Set objShell = Nothing
End Sub

```




