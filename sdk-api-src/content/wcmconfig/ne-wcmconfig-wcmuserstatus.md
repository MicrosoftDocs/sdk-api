---
UID: NE:wcmconfig.__MIDL___MIDL_itf_wcmconfig_0000_0000_0006
title: WcmUserStatus (wcmconfig.h)
description: Describes the status of the user.helpviewer_keywords: ["UnknownStatus","UserLoaded","UserRegistered","UserUnloaded","UserUnregistered","WcmUserStatus","WcmUserStatus enumeration [SMI]","smi.wcmuserstatus","wcmconfig/UnknownStatus","wcmconfig/UserLoaded","wcmconfig/UserRegistered","wcmconfig/UserUnloaded","wcmconfig/UserUnregistered","wcmconfig/WcmUserStatus"]
old-location: smi\wcmuserstatus.htm
tech.root: SMI
ms.assetid: 1a21d53f-cc0d-48ac-8d38-c53d5ac09878
ms.date: 12/05/2018
ms.keywords: UnknownStatus, UserLoaded, UserRegistered, UserUnloaded, UserUnregistered, WcmUserStatus, WcmUserStatus enumeration [SMI], smi.wcmuserstatus, wcmconfig/UnknownStatus, wcmconfig/UserLoaded, wcmconfig/UserRegistered, wcmconfig/UserUnloaded, wcmconfig/UserUnregistered, wcmconfig/WcmUserStatus
f1_keywords:
- wcmconfig/WcmUserStatus
dev_langs:
- c++
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- WcmConfig.h
api_name:
- WcmUserStatus
targetos: Windows
req.typenames: WcmUserStatus
req.redist: 
ms.custom: 19H1
---

# WcmUserStatus enumeration


## -description


Describes the status of the user.


## -enum-fields




### -field UnknownStatus

Indicates a problem with the store.


### -field UserRegistered

Indicates that the store is registered, but is not currently loaded for use.


### -field UserUnregistered

Indicates that the store does not currently exist.


### -field UserLoaded

Indicates that the store is registered, loaded, and ready for use.


### -field UserUnloaded

This has the same semantics as <b>UserRegistered</b>.


## -remarks



<b>UserUnloaded</b>, <b>UserUnregistered</b>, and <b>UnknownStatus</b> should not appear in typical use.



