---
UID: NF:shldisp.IShellDispatch2.GetSystemInformation
title: IShellDispatch2::GetSystemInformation
author: windows-sdk-content
description: Retrieves system information.
old-location: shell\IShellDispatch2_GetSystemInformation.htm
old-project: shell
ms.assetid: 57c066e3-080f-4ecc-b56e-877f0569e901
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: GetSystemInformation, GetSystemInformation method [Windows Shell], GetSystemInformation method [Windows Shell],IShellDispatch2 object, IShellDispatch2 object [Windows Shell],GetSystemInformation method, IShellDispatch2.GetSystemInformation, IShellDispatch2::GetSystemInformation, _win32_IShellDispatch2_GetSystemInformation, shell.IShellDispatch2_GetSystemInformation
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
 - IShellDispatch2.GetSystemInformation
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch2::GetSystemInformation


## -description


Retrieves system information.


## -parameters




### -param name




### -param pv






#### - sName [in]

Type: <b><a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a></b>

A <b>String</b> that specifies the system information that is being requested.


## -returns



<h3>JScript</h3>
Type: <b>Variant</b>

Returns the value of the requested system information. The return type depends on which system information is requested. See the Remarks section for details.

<h3>VB</h3>
Type: <b>Variant</b>

Returns the value of the requested system information. The return type depends on which system information is requested. See the Remarks section for details.




## -remarks



This method is implemented and accessed through the <a href="https://msdn.microsoft.com/94C10DD6-FE49-4dd4-AEED-69B73A75EDEF">Shell.GetSystemInformation</a> method.

This method can be used to request many system information values. The following table gives the <i>sName</i> value that is used to request the information and the associated type of the returned value.

                


<table class="clsStd">
<tr>
<th><i>sName</i></th>
<th>Return type</th>
<th>Description</th>
</tr>
<tr>
<td>DirectoryServiceAvailable</td>
<td><b>Boolean</b></td>
<td>Set to <b>true</b> if the directory service is available; otherwise, <b>false</b>.</td>
</tr>
<tr>
<td>DoubleClickTime</td>
<td><b>Integer</b></td>
<td>The double-click time, in milliseconds.</td>
</tr>
<tr>
<td>ProcessorLevel</td>
<td><b>Integer</b></td>
<td><b>Windows Vista and later</b>. The processor level. Returns 3, 4, or 5, for x386, x486, and Pentium-level processors, respectively.</td>
</tr>
<tr>
<td>ProcessorSpeed</td>
<td><b>Integer</b></td>
<td>The processor speed, in megahertz (MHz).</td>
</tr>
<tr>
<td>ProcessorArchitecture</td>
<td><b>Integer</b></td>
<td>The processor architecture. For details, see the discussion of the <b>wProcessorArchitecture</b> member of the <a href="https://msdn.microsoft.com/971293b8-0af0-4bdf-a7d7-6b1bb80a469c">SYSTEM_INFO</a> structure.</td>
</tr>
<tr>
<td>PhysicalMemoryInstalled</td>
<td><b>Integer</b></td>
<td>The amount of physical memory installed, in bytes.</td>
</tr>
<tr>
<td colspan="3">The following are valid only on Windows XP.</td>
</tr>
<tr>
<td>IsOS_Professional</td>
<td><b>Boolean</b></td>
<td>Set to <b>true</b> if the operating system is Windows XP Professional Edition; otherwise, <b>false</b>.</td>
</tr>
<tr>
<td>IsOS_Personal</td>
<td><b>Boolean</b></td>
<td>Set to <b>true</b> if the operating system is Windows XP Home Edition; otherwise, <b>false</b>.</td>
</tr>
<tr>
<td colspan="3">The following is valid only on Windows XP and later.</td>
</tr>
<tr>
<td>IsOS_DomainMember</td>
<td><b>Boolean</b></td>
<td>Set to <b>true</b> if the computer is a member of a domain; otherwise, <b>false</b>.</td>
</tr>
</table>
 



This method is not currently available in Microsoft Visual Basic.


#### Examples

The following examples show the use of <b>GetSystemInformation</b> for JScript and VBScript.

JScript:
                

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>&lt;script language="JavaScript"&gt;
    function fnGetSystemInformationJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;

        vReturn = objShell.GetSystemInformation("ProcessorLevel");
        document.write(vReturn);
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
    function fnGetSystemInformationVB()
        dim objShell
        dim vReturn

        set objShell = CreateObject("shell.application")

        vReturn = objShell.GetSystemInformation("ProcessorLevel")
        document.write(vReturn)

        set objShell = nothing
    end function
&lt;/script&gt;
</pre>
</td>
</tr>
</table></span></div>


