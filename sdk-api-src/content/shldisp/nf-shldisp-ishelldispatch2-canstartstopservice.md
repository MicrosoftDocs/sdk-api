---
UID: NF:shldisp.IShellDispatch2.CanStartStopService
title: IShellDispatch2::CanStartStopService
author: windows-sdk-content
description: Determines if the current user can start and stop the named service.
old-location: shell\IShellDispatch2_CanStartStopService.htm
old-project: shell
ms.assetid: cbb54ae9-02e6-4243-a782-e9f125c21c0d
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: CanStartStopService, CanStartStopService method [Windows Shell], CanStartStopService method [Windows Shell],IShellDispatch2 object, IShellDispatch2 object [Windows Shell],CanStartStopService method, IShellDispatch2.CanStartStopService, IShellDispatch2::CanStartStopService, _win32_IShellDispatch2_CanStartStopService, shell.IShellDispatch2_CanStartStopService
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
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IShellDispatch2.CanStartStopService
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch2::CanStartStopService


## -description


Determines if the current user can start and stop the named service.


## -parameters




### -param ServiceName




### -param pCanStartStop






#### - sServiceName [in]

Type: <b>String</b>

A <b>String</b> that contains the name of the service.


## -returns



<h3>JScript</h3>
Type: <b>Variant*</b>

Returns <b>true</b> if the user can start and stop the service; otherwise, <b>false</b>.

<h3>VB</h3>
Type: <b>Variant*</b>

Returns <b>true</b> if the user can start and stop the service; otherwise, <b>false</b>.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/1428F529-61F6-4113-A553-2C0D617FD859">Shell.CanStartStopService</a> method.

This method is not currently available in Microsoft Visual Basic.


#### Examples

The following examples show the usage of <b>CanStartStopService</b> for JScript and VBScript.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnCanStartStopServiceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;

        bReturn = objShell.CanStartStopService("service name");
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
    function fnCanStartStopServiceVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.CanStartStopService("service name")

        set objShell = nothing
    end function
&lt;/script&gt;
</pre>
</td>
</tr>
</table></span></div>


