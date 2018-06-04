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

# IADsTSUserEx::put_TerminalServicesHomeDrive


## -description


The root drive for the user. In a network environment, this property is a string that contains a drive specification (a drive letter followed by a colon) to which the UNC path specified as the root directory is mapped.

This property is read/write.


## -parameters


## -remarks



To set a root directory in a network environment, you must first set this property and then set the <a href="https://msdn.microsoft.com/3993b664-82bb-4419-a06f-2a4e24003170">TerminalServicesHomeDirectory</a> property.


#### Examples

The following example shows a script that binds to the SAM database without credentials.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Set DSO = GetObject("WinNT:")
Set usr = DSO.OpenDSObject("WinNT://Server1/Test,user")
WScript.echo usr.TerminalServicesHomeDrive
Wscript.echo usr.TerminalServicesHomeDirectory

usr.TerminalServicesHomeDrive = "Z:"
usr.TerminalServicesHomeDirectory = "\\servername\share\path"
usr.SetInfo

WScript.echo usr.TerminalServicesHomeDrive
WScript.echo usr.TerminalServicesHomeDirectory
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7af8fe94-15db-49dc-ba4a-b79601205f59">IADsTSUserEx</a>
 

 

