---
UID: NF:wsmandisp.IWSMan.CreateSession
title: IWSMan::CreateSession
author: windows-sdk-content
description: Creates a Session object that can then be used for subsequent network operations.
old-location: winrm\iwsman_createsession.htm
old-project: winrm
ms.assetid: 0ccab9bf-f8b4-432e-92d1-b5a5d3a2dfe5
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: CreateSession, CreateSession method [Windows Remote Management], CreateSession method [Windows Remote Management],IWSMan interface, IWSMan interface [Windows Remote Management],CreateSession method, IWSMan.CreateSession, IWSMan::CreateSession, winrm.iwsman_createsession, wsmandisp/IWSMan::CreateSession
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
 - IWSMan.CreateSession
product: Windows
targetos: Windows
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSMan::CreateSession


## -description


Creates a <a href="https://msdn.microsoft.com/b98ca759-71cb-492e-8645-8766b202eb36">Session</a> object that can then be used for subsequent network operations.


## -parameters




### -param connection [in]

The protocol and service to connect to, including either IPv4 or IPv6. The format of the connection information is as follows: &lt;<i>Transport</i>&gt;&lt;<i>Address</i>&gt;&lt;<i>Suffix</i>&gt;. For examples, see Remarks. If no connection information is provided, the local computer is used.


### -param flags [in]

The session flags that specify the authentication method, such as 
     <a href="windows_remote_management_glossary.htm">Negotiate authentication</a> 
     or 
     <a href="windows_remote_management_glossary.htm">Digest authentication</a>, 
     for connecting to a remote computer. These flags also specify other session connection information, such as 
     encoding or encryption. This parameter must contain one or more of the flags in 
     <b>__WSManSessionFlags</b> for a remote connection. For more information, see 
     <a href="https://msdn.microsoft.com/5df52696-ac2c-42b7-8b0f-99a27b58575b">Session Constants</a>. No flag settings are required for a 
     connection to the WinRM service on the local computer.

If no  authentication flags are specified, Kerberos is used unless one of the following conditions is true, 
     in which case Negotiate is used:

<ul>
<li>explicit credentials are supplied and the destination host is trusted</li>
<li>the destination host is "localhost", "127.0.0.1" or "[::1]"</li>
<li>the client computer is in a workgroup and the destination host is trusted</li>
</ul>
For more information, see <a href="https://msdn.microsoft.com/97a13b07-ae7a-4d2f-8841-77a22c91b204">Authentication for Remote Connections</a> and the <i>connectionOptions</i> parameter.


### -param connectionOptions [in]

A pointer to an <a href="https://msdn.microsoft.com/940097da-c5bb-4170-a2aa-fcbbee622fe6">IWSManConnectionOptions</a> object that contains a user name and password. The default is <b>NULL</b>.


### -param session [out]

A pointer to a new <a href="https://msdn.microsoft.com/3e016080-339f-4bda-bfd2-f912e090981f">IWSManSession</a> object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




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




<a href="https://msdn.microsoft.com/4e5acfa6-9883-4716-ac69-92161c926c66">IWSMan</a>



<a href="https://msdn.microsoft.com/299d9a95-bd30-414c-996d-6633e8b7ce52">WSMan.CreateSession</a>
 

 

