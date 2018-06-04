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

