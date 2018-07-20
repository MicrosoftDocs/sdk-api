---
UID: NF:shldisp.IShellDispatch2.IsRestricted
title: IShellDispatch2::IsRestricted
author: windows-sdk-content
description: Retrieves a group's restriction setting from the registry.
old-location: shell\IShellDispatch2_IsRestricted.htm
old-project: shell
ms.assetid: 04275c5f-c3ed-4962-882f-2cce0258a9f4
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IShellDispatch2 object [Windows Shell],IsRestricted method, IShellDispatch2.IsRestricted, IShellDispatch2::IsRestricted, IsRestricted, IsRestricted method [Windows Shell], IsRestricted method [Windows Shell],IShellDispatch2 object, _win32_IShellDispatch2_IsRestricted, shell.IShellDispatch2_IsRestricted
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
 - IShellDispatch2.IsRestricted
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch2::IsRestricted


## -description


Retrieves a group's restriction setting from the registry.


## -parameters




### -param Group




### -param Restriction




### -param plRestrictValue






#### - sGroup [in]

Type: <b><a href="https://msdn.microsoft.com/library/ms221069(v=VS.85).aspx">BSTR</a></b>

A <b>String</b> that contains the group name. This value is the name of a registry subkey under which to check for the restriction.


#### - sRestriction [in]

Type: <b><a href="https://msdn.microsoft.com/library/ms221069(v=VS.85).aspx">BSTR</a></b>

A <b>String</b> that contains the restriction whose value is to be retrieved.


## -returns



<h3>JScript</h3>
Type: <b>Integer*</b>

The value of the restriction. If the specified restriction is not found, the return value is 0.

<h3>VB</h3>
Type: <b>Integer*</b>

The value of the restriction. If the specified restriction is not found, the return value is 0.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/C4B3B5C0-7445-483a-885F-5283BD4D4B39">Shell.IsRestricted</a> method.

<b>IsRestricted</b> first looks for a subkey name that matches <i>sGroup</i> under the following key.

                <pre xml:space="preserve"><b>HKEY_LOCAL_MACHINE</b>
   <b>Software</b>
      <b>Microsoft</b>
         <b>Windows</b>
            <b>CurrentVersion</b>
               <b>Policies</b></pre>


Restrictions are declared as values of the individual policy subkeys. If the restriction named in <i>sRestriction</i> is found in the subkey named in <i>sGroup</i>, <b>IsRestricted</b> returns the restriction's current value. If the restriction is not found under <b>HKEY_LOCAL_MACHINE</b>, the same subkey is checked under <b>HKEY_CURRENT_USER</b>.

This method is not currently available in Microsoft Visual Basic.


#### Examples

The following examples show the use of <b>IsRestricted</b> to retrieve the data value of the <b>undockwithoutlogon</b> restriction from the <b>System</b> subkey. Usage is shown for JScript and VBScript.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnIsRestricedJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var lReturn;
        
        lReturn = objShell.IsRestricted("system", "undockwithoutlogon");
        document.write(lReturn);
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
    function fnIsRestricedVB()
        dim objShell
        dim lReturn

        set objShell = CreateObject("shell.application")

        lReturn = objShell.IsRestricted("system", "undockwithoutlogon")
        document.write(lReturn)

        set objShell = nothing
    end function
&lt;/script&gt;
</pre>
</td>
</tr>
</table></span></div>


