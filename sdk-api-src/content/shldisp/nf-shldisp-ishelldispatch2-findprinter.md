---
UID: NF:shldisp.IShellDispatch2.FindPrinter
title: IShellDispatch2::FindPrinter
author: windows-sdk-content
description: Displays the Find Printer dialog box.
old-location: shell\IShellDispatch2_FindPrinter.htm
old-project: shell
ms.assetid: a3d1e810-f0cf-48ec-93da-5cc01117c5d4
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: FindPrinter, FindPrinter method [Windows Shell], FindPrinter method [Windows Shell],IShellDispatch2 object, IShellDispatch2 object [Windows Shell],FindPrinter method, IShellDispatch2.FindPrinter, IShellDispatch2::FindPrinter, _win32_IShellDispatch2_FindPrinter, shell.IShellDispatch2_FindPrinter
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
 - IShellDispatch2.FindPrinter
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch2::FindPrinter


## -description


Displays the <b>Find Printer</b> dialog box.


## -parameters




### -param name




### -param location




### -param model






#### - sLocation [in, optional]

Type: <b><a href="https://msdn.microsoft.com/library/ms221069(v=VS.85).aspx">BSTR</a></b>

A <b>String</b> that contains the printer location.


#### - sModel [in, optional]

Type: <b><a href="https://msdn.microsoft.com/library/ms221069(v=VS.85).aspx">BSTR</a></b>

A <b>String</b> that contains the printer model.


#### - sName [in, optional]

Type: <b><a href="https://msdn.microsoft.com/library/ms221069(v=VS.85).aspx">BSTR</a></b>

A <b>String</b> that contains the printer name.


## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/61C700CF-623B-4c99-A211-AC26A1E4AE85">Shell.FindPrinter</a> method.

If you assign strings to one or more of the optional parameters, they are displayed as default values in the associated edit control when the <b>Find Printer</b> dialog box is displayed. The user can either accept or override these values. If no value is assigned to a parameter, the associated edit box is empty and the user must enter a value.

This method is not currently available in Microsoft Visual Basic.


#### Examples

The following examples show the use of <b>FindPrinter</b> to display the <b>Find Printer</b> dialog box for a particular application. Usage is shown for JScript, VBScript, and Visual Basic.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JScript"&gt;
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
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
    function fnFindPrinterVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")
        objShell.FindPrinter()

        set objShell = nothing
    end function
&lt;/script&gt;
</pre>
</td>
</tr>
</table></span></div>


