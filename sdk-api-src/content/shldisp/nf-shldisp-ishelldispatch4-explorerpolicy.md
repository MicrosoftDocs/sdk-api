---
UID: NF:shldisp.IShellDispatch4.ExplorerPolicy
title: IShellDispatch4::ExplorerPolicy
author: windows-sdk-content
description: Gets the value for a specified Windows Internet Explorer policy.
old-location: shell\IShellDispatch4_ExplorerPolicy.htm
old-project: shell
ms.assetid: 490c3e18-b606-456a-9016-dc4f7bad2bc3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ExplorerPolicy, ExplorerPolicy method [Windows Shell], ExplorerPolicy method [Windows Shell],IShellDispatch4 object, IShellDispatch4 object [Windows Shell],ExplorerPolicy method, IShellDispatch4.ExplorerPolicy, IShellDispatch4::ExplorerPolicy, _shell_IShellDispatch4_ExplorerPolicy, shell.IShellDispatch4_ExplorerPolicy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shldisp.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - IShellDispatch4.ExplorerPolicy
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch4::ExplorerPolicy


## -description


Gets the value for a specified Windows Internet Explorer policy.


## -parameters




### -param bstrPolicyName [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms221069(v=VS.85).aspx">BSTR</a></b>

A <b>String</b> that specifies the name of the policy.


### -param pValue






## -returns



<h3>JScript</h3>
Type: <b>Variant*</b>

The value associated with the specified policy name.

<h3>VB</h3>
Type: <b>Variant*</b>

The value associated with the specified policy name.




## -remarks



Network Administrators can control and manage the computing environment of their users by setting policies.

The specified value name must be within the  
                
                <b>HKEY_CURRENT_USER</b>\<b>Software</b>\<b>Microsoft</b>\<b>Windows</b>\<b>CurrentVersion</b>\<b>Policies</b>\<b>Explorer</b> subkey. If the value name does not exist then the method returns <b>null</b>.
            


#### Examples

The following examples show the proper use of <b>ExplorerPolicy</b> for JScript, VBScript, and Visual Basic.

JScript:
                


```javascript
<script language="JScript">
    function fnIShellDispatch4ExplorerPolicyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;
        
        vReturn = objshell.ExplorerPolicy("ValueName");
        alert(vReturn);
    }
</script>

```


VBScript:


```vb
<script language="VBScript">
     function fnIShellDispatch4ExplorerPolicyVB()
        dim objShell
        dim vReturn
        
        set objShell = CreateObject("shell.application")
            vReturn = objshell.ExplorerPolicy("ValueName")
            alert(vReturn)
        set objShell = nothing
    end function
 </script>

```


Visual Basic:


```vb
Private Sub fnIShellDispatch4ExplorerPolicyVB()
    Dim objShell As Shell
    Dim vReturn  As Variant
    
    Set objShell = New Shell
        vReturn = objshell.ExplorerPolicy("ValueName")
        Debug.Print vReturn
    Set objShell = Nothing
End Sub

```




