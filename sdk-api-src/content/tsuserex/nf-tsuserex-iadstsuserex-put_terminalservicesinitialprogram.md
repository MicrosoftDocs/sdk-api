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

# IADsTSUserEx::put_TerminalServicesInitialProgram


## -description


The path and file name of the application that the user wants to start automatically when the user logs on to the Remote Desktop Session Host (RD Session Host) server.

This property is read/write.


## -parameters


## -remarks



To set an initial application to start when the user logs on, you must first set this property and then set the <a href="https://msdn.microsoft.com/66048329-ae5a-4e70-b6a4-dcdc312a74df">TerminalServicesWorkDirectory</a> property. If you set only the <b>TerminalServicesInitialProgram</b> property, the application starts in the user's session in the default user directory.


#### Examples

The following example shows a script that binds to the Active Directory database without credentials.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Set DSO = GetObject("LDAP:")
Set usr = DSO.OpenDSObject(
    "LDAP://DOMAIN/CN=Test,CN=Users,DC=Server1,DC=Domain,DC=com")
Wscript.echo usr.TerminalServicesWorkDirectory
Wscript.echo usr.TerminalServicesInitialProgram
usr.TerminalServicesInitialProgram= "cmd.exe"
usr.TerminalServicesWorkDirectory= "D:\path"
usr.SetInfo
WScript.echo usr.TerminalServicesInitialProgram
Wscript.echo usr.TerminalServicesWorkDirectory
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7af8fe94-15db-49dc-ba4a-b79601205f59">IADsTSUserEx</a>
 

 

