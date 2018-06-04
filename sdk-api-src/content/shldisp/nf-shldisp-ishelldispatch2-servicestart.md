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

# IShellDispatch2::ServiceStart


## -description


Starts a named service.


## -parameters




### -param ServiceName




### -param Persistent




### -param pSuccess






#### - sServiceName [in]

Type: <b><a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a></b>

A <b>String</b> that contains the name of the service.


#### - vPersistent [in]

Type: <b>Variant</b>

Set to <b>true</b> to have the service started automatically by the service control manager during system startup. Set to <b>false</b> to leave the service configuration unchanged.


## -returns



<h3>JScript</h3>
Type: <b>Variant*</b>

Returns <b>true</b> if successful; otherwise, <b>false</b>.

<h3>VB</h3>
Type: <b>Variant*</b>

Returns <b>true</b> if successful; otherwise, <b>false</b>.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/72214E80-38A2-4a57-B555-942902BAFC3D">Shell.ServiceStart</a> method.

The method returns <b>false</b> if the service has already been started. Before calling this method, you can call <a href="https://msdn.microsoft.com/FDC41C2D-7462-458f-BBE6-D97260C26B6C">Shell.IsServiceRunning</a> to ascertain the status of the service.

This method is not currently available in Microsoft Visual Basic.


#### Examples

The following examples show the use of <b>ServiceStart</b> to start the Messenger service. Usage is shown for JScript and VBScript.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
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
    function fnServiceStartVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStart("Messenger", true)

        set objShell = nothing
    end function
&lt;/script&gt;
</pre>
</td>
</tr>
</table></span></div>


