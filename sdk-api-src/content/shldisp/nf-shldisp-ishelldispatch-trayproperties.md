---
UID: NF:shldisp.IShellDispatch.TrayProperties
title: IShellDispatch::TrayProperties
author: windows-sdk-content
description: Displays the Taskbar and Start Menu Properties dialog box. This method has the same effect as right-clicking the taskbar and selecting Properties.
old-location: shell\IShellDispatch_TrayProperties.htm
old-project: shell
ms.assetid: 8E0AC08E-1132-4312-9B75-E7686B91AB02
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IShellDispatch object [Windows Shell],TrayProperties method, IShellDispatch.TrayProperties, IShellDispatch::TrayProperties, TrayProperties, TrayProperties method [Windows Shell], TrayProperties method [Windows Shell],IShellDispatch object, shell.IShellDispatch_TrayProperties
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
 - IShellDispatch.TrayProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch::TrayProperties


## -description


Displays the <b>Taskbar and Start Menu Properties</b> dialog box. This method has the same effect as right-clicking the taskbar and selecting <b>Properties</b>.


## -parameters






## -returns



<h3>JScript</h3>
This method does not return a value.

<h3>VB</h3>
This method does not return a value.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/0d82d847-9e6f-461e-b938-fe8fd49a636f">Shell.TrayProperties</a> method.


#### Examples

The following examples show the use of <b>TrayProperties</b> in JScript, VBScript, and Visual Basic.

JScript:
                


```javascript
<script language="JScript">
    function fnShellTrayPropertiesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TrayProperties();
    }
</script>

```


VBScript:


```vb
<script language="VBScript">
    function fnShellTrayPropertiesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TrayProperties

        set objShell = nothing
    end function
 </script>

```


Visual Basic:


```vb
Private Sub fnShellTrayPropertiesVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TrayProperties

    Set objShell = Nothing
End Sub

```




