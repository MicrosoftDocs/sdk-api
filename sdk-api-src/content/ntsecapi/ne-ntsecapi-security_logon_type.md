---
UID: NE:ntsecapi._SECURITY_LOGON_TYPE
title: SECURITY_LOGON_TYPE (ntsecapi.h)
description: Indicates the type of logon requested by a logon process.
helpviewer_keywords: ["*PSECURITY_LOGON_TYPE","Batch","CachedInteractive","CachedRemoteInteractive","CachedUnlock","Interactive","Network","NetworkCleartext","NewCredentials","PSECURITY_LOGON_TYPE","PSECURITY_LOGON_TYPE enumeration pointer [Security]","Proxy","RemoteInteractive","SECURITY_LOGON_TYPE","SECURITY_LOGON_TYPE enumeration [Security]","Service","Unlock","_lsa_security_logon_type","ntsecapi/Batch","ntsecapi/CachedInteractive","ntsecapi/CachedRemoteInteractive","ntsecapi/CachedUnlock","ntsecapi/Interactive","ntsecapi/Network","ntsecapi/NetworkCleartext","ntsecapi/NewCredentials","ntsecapi/PSECURITY_LOGON_TYPE","ntsecapi/Proxy","ntsecapi/RemoteInteractive","ntsecapi/SECURITY_LOGON_TYPE","ntsecapi/Service","ntsecapi/Unlock","security.security_logon_type"]
old-location: security\security_logon_type.htm
tech.root: security
ms.assetid: d775d782-9403-47b2-bb43-8f677db49eb9
ms.date: 12/05/2018
ms.keywords: '*PSECURITY_LOGON_TYPE, Batch, CachedInteractive, CachedRemoteInteractive, CachedUnlock, Interactive, Network, NetworkCleartext, NewCredentials, PSECURITY_LOGON_TYPE, PSECURITY_LOGON_TYPE enumeration pointer [Security], Proxy, RemoteInteractive, SECURITY_LOGON_TYPE, SECURITY_LOGON_TYPE enumeration [Security], Service, Unlock, _lsa_security_logon_type, ntsecapi/Batch, ntsecapi/CachedInteractive, ntsecapi/CachedRemoteInteractive, ntsecapi/CachedUnlock, ntsecapi/Interactive, ntsecapi/Network, ntsecapi/NetworkCleartext, ntsecapi/NewCredentials, ntsecapi/PSECURITY_LOGON_TYPE, ntsecapi/Proxy, ntsecapi/RemoteInteractive, ntsecapi/SECURITY_LOGON_TYPE, ntsecapi/Service, ntsecapi/Unlock, security.security_logon_type'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SECURITY_LOGON_TYPE, *PSECURITY_LOGON_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECURITY_LOGON_TYPE
 - ntsecapi/_SECURITY_LOGON_TYPE
 - PSECURITY_LOGON_TYPE
 - ntsecapi/PSECURITY_LOGON_TYPE
 - SECURITY_LOGON_TYPE
 - ntsecapi/SECURITY_LOGON_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - SECURITY_LOGON_TYPE
---

# SECURITY_LOGON_TYPE enumeration


## -description

The <b>SECURITY_LOGON_TYPE</b> enumeration indicates the type of logon requested by a logon process.

## -enum-fields

### -field UndefinedLogonType:0

### -field Interactive:2

The <a href="/windows/desktop/SecGloss/s-gly">security principal</a> is logging on interactively.

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
