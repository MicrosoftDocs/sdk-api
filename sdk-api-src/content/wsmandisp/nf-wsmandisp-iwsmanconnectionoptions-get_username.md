---
UID: NF:wsmandisp.IWSManConnectionOptions.get_UserName
title: IWSManConnectionOptions::get_UserName
author: windows-sdk-content
description: Sets and gets the user name of a local or a domain account on the remote computer. This property determines the user name for authentication.
old-location: winrm\connectionoptions_username.htm
old-project: WinRM
ms.assetid: e8f70143-f002-4b39-97a3-006b9713262d
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: ConnectionOptions object [Windows Remote Management],UserName property, ConnectionOptions.UserName, IWSManConnectionOptions.get_UserName, IWSManConnectionOptions.put_UserName, IWSManConnectionOptions::get_UserName, UserName property [Windows Remote Management], UserName property [Windows Remote Management],ConnectionOptions object, get_UserName, winrm.connectionoptions_username, wsman.connectionoptions_username
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSManProxyAuthenticationFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - ConnectionOptions.UserName
 - IWSManConnectionOptions.get_UserName
 - IWSManConnectionOptions.put_UserName
product: Windows
targetos: Windows
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSManConnectionOptions::get_UserName


## -description


Sets and gets the user name of a local or a domain account on the remote computer. This property determines the user name for authentication. For more information, see <a href="https://msdn.microsoft.com/97a13b07-ae7a-4d2f-8841-77a22c91b204">Authentication for Remote Connections</a>.

This property is read/write.


## -parameters


## -remarks



The following syntax is used to specify this property.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Set ConnectionOptions = wsman.CreateConnectionOptions
ConnectionOptions.UserName = "&lt;UserName&gt;"</pre>
</td>
</tr>
</table></span></div>
You can supply <b>UserName</b> and <a href="https://msdn.microsoft.com/library/windows/hardware/dn915695">Password</a> for a domain account when using <a href="windows_remote_management_glossary.htm">negotiate</a> or <i>Kerberos</i> authentication, or for a local account with <a href="windows_remote_management_glossary.htm">Basic</a> authentication.  To connect to a local account, the <a href="https://msdn.microsoft.com/299d9a95-bd30-414c-996d-6633e8b7ce52">WSMan.CreateSession</a> flags must contain the combination of the <b>WSManFlagUseBasic</b>
flag and  the <b>WsmanFlagCredUserNamePassword</b> flag. To connect to a domain account, the <b>WSMan.CreateSession</b> flags must contain the combination of the <b>WSManFlagUseNegotiate</b>
flag and  the <b>WsmanFlagCredUserNamePassword</b> flag, or the combination of the <b>WSManFlagUseKerberos</b>
flag and  the <b>WsmanFlagCredUserNamePassword</b> flag. For a domain account, <b>UserName</b> must be specified in the form "computer\username", where the "computer" part of the string can be either the name or the IP address. For more information, see <a href="https://msdn.microsoft.com/97a13b07-ae7a-4d2f-8841-77a22c91b204">Authentication for Remote Connections</a>.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseBasic Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
</pre>
</td>
</tr>
</table></span></div>
For connecting to a domain account, the  <a href="https://msdn.microsoft.com/299d9a95-bd30-414c-996d-6633e8b7ce52">WSMan.CreateSession</a> flags must contain the combination of the <b>WSManFlagUseNegotiate</b>
flag and  the <b>WsmanFlagCredUserNamePassword</b> flag for connecting to a domain account, which requires Negotiate authentication.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseNegotiate Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7a87a5f7-78ed-452c-9b9f-ad48811a3339">ConnectionOptions</a>
 

 

