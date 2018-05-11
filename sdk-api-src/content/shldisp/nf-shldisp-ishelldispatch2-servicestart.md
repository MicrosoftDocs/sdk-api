---
UID: NF:shldisp.IShellDispatch2.ServiceStart
title: IShellDispatch2::ServiceStart
author: windows-driver-content
description: Starts a named service.
old-location: shell\IShellDispatch2_ServiceStart.htm
old-project: shell
ms.assetid: 3af57cdc-f449-433d-a9e1-119038045e4c
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IShellDispatch2 object [Windows Shell],ServiceStart method, IShellDispatch2.ServiceStart, IShellDispatch2::ServiceStart, ServiceStart, ServiceStart method [Windows Shell], ServiceStart method [Windows Shell],IShellDispatch2 object, _win32_IShellDispatch2_ServiceStart, shell.IShellDispatch2_ServiceStart
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IShellDispatch2.ServiceStart
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
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


