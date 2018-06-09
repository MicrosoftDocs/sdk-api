---
UID: NF:tsuserex.IADsTSUserEx.get_TerminalServicesHomeDrive
title: IADsTSUserEx::get_TerminalServicesHomeDrive
author: windows-sdk-content
description: The root drive for the user. In a network environment, this property is a string that contains a drive specification (a drive letter followed by a colon) to which the UNC path specified as the root directory is mapped.
old-location: termserv\iadstsuserex_terminalserviceshomedrive.htm
old-project: TermServ
ms.assetid: e5cfa526-eff8-4a89-9b13-c4a06a416fe5
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IADsTSUserEx interface [Remote Desktop Services],TerminalServicesHomeDrive property, IADsTSUserEx.TerminalServicesHomeDrive, IADsTSUserEx.get_TerminalServicesHomeDrive, IADsTSUserEx::TerminalServicesHomeDrive, IADsTSUserEx::get_TerminalServicesHomeDrive, IADsTSUserEx::put_TerminalServicesHomeDrive, TerminalServicesHomeDrive property [Remote Desktop Services], TerminalServicesHomeDrive property [Remote Desktop Services],IADsTSUserEx interface, get_TerminalServicesHomeDrive, termserv.iadstsuserex_terminalserviceshomedrive, tsuserex/IADsTSUserEx::TerminalServicesHomeDrive, tsuserex/IADsTSUserEx::get_TerminalServicesHomeDrive, tsuserex/IADsTSUserEx::put_TerminalServicesHomeDrive
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tsuserex.h
req.include-header: Tsuserex.h, Tsuserex_i.c
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Tsuserex.tlb
tech.root: 
req.typenames: WTSSBX_SESSION_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tsuserex.dll
api_name:
 - IADsTSUserEx.TerminalServicesHomeDrive
 - IADsTSUserEx.get_TerminalServicesHomeDrive
 - IADsTSUserEx.put_TerminalServicesHomeDrive
product: Windows
targetos: Windows
req.lib: 
req.dll: Tsuserex.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IADsTSUserEx::get_TerminalServicesHomeDrive


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
 

 

