---
UID: NF:shldisp.IShellDispatch2.IsServiceRunning
title: IShellDispatch2::IsServiceRunning
author: windows-sdk-content
description: Returns a value that indicates whether a particular service is running.
old-location: shell\IShellDispatch2_IsServiceRunning.htm
old-project: shell
ms.assetid: 91f3fba1-7aa5-423a-bc37-49db230c79db
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IShellDispatch2 object [Windows Shell],IsServiceRunning method, IShellDispatch2.IsServiceRunning, IShellDispatch2::IsServiceRunning, IsServiceRunning, IsServiceRunning method [Windows Shell], IsServiceRunning method [Windows Shell],IShellDispatch2 object, _win32_IShellDispatch2_IsServiceRunning, shell.IShellDispatch2_IsServiceRunning
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
 - IShellDispatch2.IsServiceRunning
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch2::IsServiceRunning


## -description


Returns a value that indicates whether a particular service is running.


## -parameters




### -param ServiceName




### -param pRunning






#### - sServiceName [in]

Type: <b><a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a></b>

A <b>String</b> that contains the name of the service.


## -returns



<h3>JScript</h3>
Type: <b>Variant*</b>

Returns <b>true</b> if the service specified by <i>sServiceName</i> is running; otherwise, <b>false</b>.

<h3>VB</h3>
Type: <b>Variant*</b>

Returns <b>true</b> if the service specified by <i>sServiceName</i> is running; otherwise, <b>false</b>.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/FDC41C2D-7462-458f-BBE6-D97260C26B6C">Shell.IsServiceRunning</a> method.

This method is not currently available in Microsoft Visual Basic.


#### Examples

The following examples show the use of <b>IsServiceRunning</b> to determine whether the Themes service is running for an application. Usage is shown for JScript and VBScript.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnIsServiceRunningJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
    
        bReturn = objShell.IsServiceRunning("Themes");
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
    function fnIsServiceRunningVB()
        dim objShell
        dim bReturn
    
        set objShell = CreateObject("shell.application")
    
        bReturn = objShell.IsServiceRunning("Themes")
    
        set objShell = nothing
    end function
&lt;/script&gt;
</pre>
</td>
</tr>
</table></span></div>


