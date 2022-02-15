---
UID: NF:wsmandisp.IWSMan.CreateSession
title: IWSMan::CreateSession (wsmandisp.h)
description: Creates a Session object that can then be used for subsequent network operations.
helpviewer_keywords: ["CreateSession","CreateSession method [Windows Remote Management]","CreateSession method [Windows Remote Management]","IWSMan interface","IWSMan interface [Windows Remote Management]","CreateSession method","IWSMan.CreateSession","IWSMan::CreateSession","winrm.iwsman_createsession","wsmandisp/IWSMan::CreateSession"]
old-location: winrm\iwsman_createsession.htm
tech.root: winrm
ms.assetid: 0ccab9bf-f8b4-432e-92d1-b5a5d3a2dfe5
ms.date: 12/05/2018
ms.keywords: CreateSession, CreateSession method [Windows Remote Management], CreateSession method [Windows Remote Management],IWSMan interface, IWSMan interface [Windows Remote Management],CreateSession method, IWSMan.CreateSession, IWSMan::CreateSession, winrm.iwsman_createsession, wsmandisp/IWSMan::CreateSession
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
 - IWSMan::CreateSession
 - wsmandisp/IWSMan::CreateSession
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
 - IWSMan.CreateSession
---

# IWSMan::CreateSession


## -description

Creates a <a href="/windows/desktop/WinRM/session">Session</a> object that can then be used for subsequent network operations.

## -parameters

### -param connection [in]

The protocol and service to connect to, including either IPv4 or IPv6. The format of the connection information is as follows: &lt;<i>Transport</i>&gt;&lt;<i>Address</i>&gt;&lt;<i>Suffix</i>&gt;. For examples, see Remarks. If no connection information is provided, the local computer is used.

### -param flags [in]

The session flags that specify the authentication method, such as 
     <a href="/windows/desktop/WinRM/windows-remote-management-glossary">Negotiate authentication</a> 
     or 
     <a href="/windows/desktop/WinRM/windows-remote-management-glossary">Digest authentication</a>, 
     for connecting to a remote computer. These flags also specify other session connection information, such as 
     encoding or encryption. This parameter must contain one or more of the flags in 
     <b>__WSManSessionFlags</b> for a remote connection. For more information, see 
     <a href="/windows/desktop/WinRM/session-constants">Session Constants</a>. No flag settings are required for a 
     connection to the WinRM service on the local computer.

If no  authentication flags are specified, Kerberos is used unless one of the following conditions is true, 
     in which case Negotiate is used:

<ul>
<li>explicit credentials are supplied and the destination host is trusted</li>
<li>the destination host is "localhost", "127.0.0.1" or "[::1]"</li>
<li>the client computer is in a workgroup and the destination host is trusted</li>
</ul>
For more information, see <a href="/windows/desktop/WinRM/authentication-for-remote-connections">Authentication for Remote Connections</a> and the <i>connectionOptions</i> parameter.

### -param connectionOptions [in]

A pointer to an <a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanconnectionoptions">IWSManConnectionOptions</a> object that contains a user name and password. The default is <b>NULL</b>.

### -param session [out]

A pointer to a new <a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmansession">IWSManSession</a> object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The following list contains examples of formats used to specify connection information in the <i>connection</i> parameter (when creating an HTTPS session, the &lt;<i>Address</i>&gt; field must match the server computer certificate name, otherwise a failure occurs):

<ul>
<li>
"https://service"

Uses HTTPS to connect to the default web service location.

</li>
<li>
"https://service.corp.com/websvcs/wsman"

Uses HTTPS to connect to the specific web service location.

</li>
<li>
"https://[E3D7:0000:0000:0000:51F4:9BC8:C0A8:6420]"

Uses HTTPS and IPv6 with the default port.

</li>
<li>
"https://[E3D7:0000:0000:0000:51F4:9BC8:C0A8:6420]:9999/wsman"

Uses HTTPS and IPv6 with the given port.

</li>
</ul>

## -see-also

<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsman">IWSMan</a>



<a href="/windows/desktop/WinRM/wsman-createsession">WSMan.CreateSession</a>