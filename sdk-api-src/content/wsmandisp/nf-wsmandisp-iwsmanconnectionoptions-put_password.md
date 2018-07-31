---
UID: NF:wsmandisp.IWSManConnectionOptions.put_Password
title: IWSManConnectionOptions::put_Password
author: windows-sdk-content
description: Sets the password of a local or a domain account on the remote computer. This property determines the password for authentication.
old-location: winrm\connectionoptions_password.htm
old-project: WinRM
ms.assetid: 61ba54b6-7da0-423e-b5b2-c4dd8aacd042
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ConnectionOptions object [Windows Remote Management],Password property, ConnectionOptions.Password, IWSManConnectionOptions.get_Password, IWSManConnectionOptions.put_Password, IWSManConnectionOptions::put_Password, Password property [Windows Remote Management], Password property [Windows Remote Management],ConnectionOptions object, put_Password, winrm.connectionoptions_password, wsman.connectionoptions_password
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
 - ConnectionOptions.Password
 - IWSManConnectionOptions.get_Password
 - IWSManConnectionOptions.put_Password
product: Windows
targetos: Windows
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSManConnectionOptions::put_Password


## -description


Sets the password of a local or a domain account on the remote computer. This property determines the password for authentication. For more information, see <a href="https://msdn.microsoft.com/97a13b07-ae7a-4d2f-8841-77a22c91b204">Authentication for Remote Connections</a>.

This property is read/write.


## -parameters


## -remarks



Be aware that you cannot retrieve the password. The password can only be set with this property.

If you create a <a href="https://msdn.microsoft.com/7a87a5f7-78ed-452c-9b9f-ad48811a3339">ConnectionOptions</a> object and use a user name and password to connect to Windows Remote Management, then the <b>WSManFlagCredUserNamePassword</b> flag should be set on the call to <a href="https://msdn.microsoft.com/299d9a95-bd30-414c-996d-6633e8b7ce52">WSMan.CreateSession</a>.

For more information about setting passwords, see the Remarks section in <a href="https://msdn.microsoft.com/7a87a5f7-78ed-452c-9b9f-ad48811a3339">ConnectionOptions</a>.


#### Examples

The following code example creates a <a href="https://msdn.microsoft.com/7a87a5f7-78ed-452c-9b9f-ad48811a3339">ConnectionOptions</a> object and sets the <b>Password</b>.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>' Create a WSMan object. 
Set objWsman = CreateObject( "WSMAN.Automation" )
' Create a ConnectionOptions object
Set objOptions = objWSMan.CreateConnectionOptions
objOptions.Password = "&lt;password&gt;"</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7a87a5f7-78ed-452c-9b9f-ad48811a3339">ConnectionOptions</a>
 

 

