---
UID: NF:shldisp.IShellDispatch2.ServiceStop
title: IShellDispatch2::ServiceStop
author: windows-sdk-content
description: Stops a named service.
old-location: shell\IShellDispatch2_ServiceStop.htm
old-project: shell
ms.assetid: f4cd0e2c-4ecc-4e9f-a0b5-d2a8a739f0e2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IShellDispatch2 object [Windows Shell],ServiceStop method, IShellDispatch2.ServiceStop, IShellDispatch2::ServiceStop, ServiceStop, ServiceStop method [Windows Shell], ServiceStop method [Windows Shell],IShellDispatch2 object, _win32_IShellDispatch2_ServiceStop, shell.IShellDispatch2_ServiceStop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shldisp.h
req.include-header: 
req.redist: 
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
 - IShellDispatch2.ServiceStop
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch2::ServiceStop


## -description


Stops a named service.


## -parameters




### -param ServiceName




### -param Persistent




### -param pSuccess






#### - sServiceName [in]

Type: <b><a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a></b>

A <b>String</b> that contains the name of the service.


#### - vPersistent [in]

Type: <b>Variant</b>

Set to <b>true</b> to have the service started by the service control manager when <a href="https://msdn.microsoft.com/3af57cdc-f449-433d-a9e1-119038045e4c">ServiceStart</a> is called. To leave the service configuration unchanged, set <i>vPersistent</i> to <b>false</b>.


## -returns



<h3>JScript</h3>
Type: <b>Variant*</b>

Returns <b>true</b> if successful; otherwise, <b>false</b>.

<h3>VB</h3>
Type: <b>Variant*</b>

Returns <b>true</b> if successful; otherwise, <b>false</b>.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/AC22C91E-BBC6-4a2e-8D39-F9D7C0AC0947">Shell.ServiceStop</a> method.

The method returns <b>false</b> if the service has already been stopped. Before calling this method, you can call <a href="https://msdn.microsoft.com/FDC41C2D-7462-458f-BBE6-D97260C26B6C">Shell.IsServiceRunning</a> to ascertain the status of the service.

This method is not currently available in Microsoft Visual Basic.


#### Examples

The following examples show the use of <b>ServiceStop</b> to stop the Messenger service. Usage is shown for JScript and VBScript.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnServiceStopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStop("Messenger", true);
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
    function fnServiceStopVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStop("Messenger", true)

        set objShell = nothing
    end function
&lt;/script&gt;
</pre>
</td>
</tr>
</table></span></div>


