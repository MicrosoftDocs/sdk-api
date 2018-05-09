---
UID: NE:ntsecapi._SECURITY_LOGON_TYPE
title: "_SECURITY_LOGON_TYPE"
author: windows-driver-content
description: Indicates the type of logon requested by a logon process.
old-location: security\security_logon_type.htm
old-project: SecAuthN
ms.assetid: d775d782-9403-47b2-bb43-8f677db49eb9
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: "*PSECURITY_LOGON_TYPE, Batch, CachedInteractive, CachedRemoteInteractive, CachedUnlock, Interactive, Network, NetworkCleartext, NewCredentials, PSECURITY_LOGON_TYPE, PSECURITY_LOGON_TYPE enumeration pointer [Security], Proxy, RemoteInteractive, SECURITY_LOGON_TYPE, SECURITY_LOGON_TYPE enumeration [Security], Service, Unlock, _SECURITY_LOGON_TYPE, _lsa_security_logon_type, ntsecapi/Batch, ntsecapi/CachedInteractive, ntsecapi/CachedRemoteInteractive, ntsecapi/CachedUnlock, ntsecapi/Interactive, ntsecapi/Network, ntsecapi/NetworkCleartext, ntsecapi/NewCredentials, ntsecapi/PSECURITY_LOGON_TYPE, ntsecapi/Proxy, ntsecapi/RemoteInteractive, ntsecapi/SECURITY_LOGON_TYPE, ntsecapi/Service, ntsecapi/Unlock, security.security_logon_type"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SECURITY_LOGON_TYPE, *PSECURITY_LOGON_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntsecapi.h
api_name:
-	SECURITY_LOGON_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _SECURITY_LOGON_TYPE enumeration


## -description


The <b>SECURITY_LOGON_TYPE</b> enumeration indicates the type of logon requested by a logon process.


## -enum-fields




### -field UndefinedLogonType


### -field Interactive

The <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security principal</a> is logging on interactively.


### -field Network

The security principal is logging using a network.


### -field Batch

The logon is for a batch process.


### -field Service

The logon is for a service account.


### -field Proxy

Not supported.


### -field Unlock

The logon is an attempt to unlock a workstation.


### -field NetworkCleartext

The logon is a network logon with plaintext credentials.


### -field NewCredentials

Allows the caller to clone its current token and specify new credentials for outbound connections. The new logon session has the same local identity but uses different credentials for other network connections.


### -field RemoteInteractive

A terminal server session that is both remote and interactive.


### -field CachedInteractive

Attempt to use the cached credentials without going out across the network.


### -field CachedRemoteInteractive

Same as <b>RemoteInteractive</b>, except used internally for auditing purposes.


### -field CachedUnlock

The logon is an attempt to unlock a workstation.

