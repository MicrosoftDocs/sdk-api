---
UID: NF:wsmandisp.IWSManConnectionOptions.put_UserName
title: IWSManConnectionOptions::put_UserName (wsmandisp.h)
description: Sets and gets the user name of a local or a domain account on the remote computer. This property determines the user name for authentication. (Put)
helpviewer_keywords: ["IWSManConnectionOptions interface [Windows Remote Management]","UserName property","IWSManConnectionOptions.UserName","IWSManConnectionOptions.put_UserName","IWSManConnectionOptions::UserName","IWSManConnectionOptions::get_UserName","IWSManConnectionOptions::put_UserName","UserName property [Windows Remote Management]","UserName property [Windows Remote Management]","IWSManConnectionOptions interface","put_UserName","winrm.iwsmanconnectionoptions_username","wsmandisp/IWSManConnectionOptions::UserName","wsmandisp/IWSManConnectionOptions::get_UserName","wsmandisp/IWSManConnectionOptions::put_UserName"]
old-location: winrm\iwsmanconnectionoptions_username.htm
tech.root: winrm
ms.assetid: 7b20fcac-0481-4619-aa57-f72318a9a68d
ms.date: 12/05/2018
ms.keywords: IWSManConnectionOptions interface [Windows Remote Management],UserName property, IWSManConnectionOptions.UserName, IWSManConnectionOptions.put_UserName, IWSManConnectionOptions::UserName, IWSManConnectionOptions::get_UserName, IWSManConnectionOptions::put_UserName, UserName property [Windows Remote Management], UserName property [Windows Remote Management],IWSManConnectionOptions interface, put_UserName, winrm.iwsmanconnectionoptions_username, wsmandisp/IWSManConnectionOptions::UserName, wsmandisp/IWSManConnectionOptions::get_UserName, wsmandisp/IWSManConnectionOptions::put_UserName
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
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSManConnectionOptions::put_UserName
 - wsmandisp/IWSManConnectionOptions::put_UserName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManConnectionOptions.UserName
 - IWSManConnectionOptions.get_UserName
 - IWSManConnectionOptions.put_UserName
---

# IWSManConnectionOptions::put_UserName


## -description

Sets and gets the user name of a local or a domain account on the remote computer. This property determines the user name for authentication. If no value is supplied and the <b>WSManFlagCredUsernamePassword</b> flag is not set, then the user name of the account that is running the script is used.

 If the <b>WSManFlagCredUsernamePassword</b> flag is set but no user name is specified, the script prompts the user to enter the user name and password. If no user name and password are entered then an access denied error is returned. For more information, see <a href="/windows/desktop/WinRM/authentication-for-remote-connections">Authentication for Remote Connections</a>.

This property is read/write.

## -parameters

## -remarks

You can supply <a href="/windows/desktop/WinRM/connectionoptions-username">UserName</a> and <a href="/windows/desktop/WinRM/connectionoptions-password">Password</a> for a domain account when using <a href="/windows/desktop/WinRM/windows-remote-management-glossary">Negotiate</a> or <i>Kerberos</i> authentication, or for a local account with <a href="/windows/desktop/WinRM/windows-remote-management-glossary">Basic</a> authentication.  To connect to a local account, the <a href="/windows/desktop/WinRM/wsman-createsession">WSMan.CreateSession</a> flags must contain the combination of the <b>WSManFlagUseBasic</b> flag and  the <b>WsmanFlagCredUserNamePassword</b> flag. To connect to a domain account, the <b>WSMan.CreateSession</b> flags must contain the combination of the <b>WSManFlagUseNegotiate</b> flag and  the <b>WsmanFlagCredUserNamePassword</b> flag, or the combination of the <b>WSManFlagUseKerberos</b> flag and  the <b>WsmanFlagCredUserNamePassword</b> flag. For a domain account, <b>UserName</b> must be specified in the form "computer\username", where the "computer" part of the string can be either the name or the IP address. For more information, see <a href="/windows/desktop/WinRM/authentication-for-remote-connections">Authentication for Remote Connections</a>.

## -see-also

<a href="/windows/desktop/WinRM/connectionoptions-username">ConnectionOptions.UserName</a>



<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanconnectionoptions">IWSManConnectionOptions</a>
