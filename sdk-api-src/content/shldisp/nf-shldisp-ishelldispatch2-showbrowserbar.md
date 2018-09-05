---
UID: NF:shldisp.IShellDispatch2.ShowBrowserBar
title: IShellDispatch2::ShowBrowserBar
author: windows-sdk-content
description: Displays a browser bar.
old-location: shell\IShellDispatch2_ShowBrowserBar.htm
old-project: shell
ms.assetid: 5776370c-3bbf-449b-a8fe-2dbc7d89dd25
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IShellDispatch2 object [Windows Shell],ShowBrowserBar method, IShellDispatch2.ShowBrowserBar, IShellDispatch2::ShowBrowserBar, ShowBrowserBar, ShowBrowserBar method [Windows Shell], ShowBrowserBar method [Windows Shell],IShellDispatch2 object, _win32_IShellDispatch2_ShowBrowserBar, shell.IShellDispatch2_ShowBrowserBar
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
 - IShellDispatch2.ShowBrowserBar
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch2::ShowBrowserBar


## -description


Displays a browser bar.


## -parameters




### -param bstrClsid




### -param bShow




### -param pSuccess






#### - sCLSID [in]

Type: <b><a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a></b>

A <b>String</b> that contains the string form of the CLSID of the browser bar to be displayed. The object must be registered as an Explorer Bar object with a CATID_InfoBand component category. For further information, see <a href="https://msdn.microsoft.com/4bf46b3f-f833-42e0-baf7-21bfa9e6d890">Creating Custom Explorer Bars, Tool Bands, and Desk Bands</a>.


#### - vShow [in]

Type: <b>Variant</b>

Set to <b>true</b> to show the browser bar or <b>false</b> to hide it.


## -returns



<h3>JScript</h3>
Type: <b>Variant*</b>

Returns <b>true</b> if successful; otherwise, <b>false</b>.

<h3>VB</h3>
Type: <b>Variant*</b>

Returns <b>true</b> if successful; otherwise, <b>false</b>.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/203636D2-54D3-4163-B9AC-39213D6F4203">Shell.ShowBrowserBar</a> method.

You can display one of the standard Explorer Bars by setting the <i>sCLSID</i> parameter to the CLSID of that Explorer Bar. The standard Explorer Bars and their CLSID strings are as follows:

                


<table class="clsStd">
<tr>
<th>Explorer Bar</th>
<th>CLSID string
                            </th>
</tr>
<tr>
<td>Favorites</td>
<td>{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</td>
</tr>
<tr>
<td>Folders</td>
<td>{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</td>
</tr>
<tr>
<td>History</td>
<td>{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</td>
</tr>
<tr>
<td>Search</td>
<td>{30D02401-6A81-11d0-8274-00C04FD5AE38}</td>
</tr>
</table>
 



This method is not currently available in Microsoft Visual Basic.


#### Examples

The following examples show the use of <b>ShowBrowserBar</b> to display the <b>Favorites</b> browser bar. Usage is shown for JScript and VBScript.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JavaScript"&gt;
    function fnShowBrowserBarJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true);
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
    function fnShowBrowserBarVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true)

        set objShell = nothing
    end function
&lt;/script&gt;
</pre>
</td>
</tr>
</table></span></div>


