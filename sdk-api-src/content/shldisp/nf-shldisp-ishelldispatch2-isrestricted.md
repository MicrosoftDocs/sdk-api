---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IShellDispatch2::IsRestricted


## -description


Retrieves a group's restriction setting from the registry.


## -parameters




### -param Group




### -param Restriction




### -param plRestrictValue






#### - sGroup [in]

Type: <b><a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a></b>

A <b>String</b> that contains the group name. This value is the name of a registry subkey under which to check for the restriction.


#### - sRestriction [in]

Type: <b><a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a></b>

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


