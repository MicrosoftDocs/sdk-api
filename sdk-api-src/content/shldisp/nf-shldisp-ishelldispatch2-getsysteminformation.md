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


