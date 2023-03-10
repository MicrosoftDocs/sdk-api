---
UID: NF:azroles.IAzAuthorizationStore.get_DomainTimeout
title: IAzAuthorizationStore::get_DomainTimeout (azroles.h)
description: Sets or retrieves the time in milliseconds after which a domain is determined to be unreachable. (Get)
helpviewer_keywords: ["AzAuthorizationStore object [Security]","DomainTimeout property","DomainTimeout property [Security]","DomainTimeout property [Security]","AzAuthorizationStore object","DomainTimeout property [Security]","IAzAuthorizationStore interface","IAzAuthorizationStore interface [Security]","DomainTimeout property","IAzAuthorizationStore.DomainTimeout","IAzAuthorizationStore.get_DomainTimeout","IAzAuthorizationStore::DomainTimeout","IAzAuthorizationStore::get_DomainTimeout","IAzAuthorizationStore::put_DomainTimeout","azroles/IAzAuthorizationStore::DomainTimeout","azroles/IAzAuthorizationStore::get_DomainTimeout","azroles/IAzAuthorizationStore::put_DomainTimeout","get_DomainTimeout","security.azauthorizationstore_domaintimeout"]
old-location: security\azauthorizationstore_domaintimeout.htm
tech.root: security
ms.assetid: e512641d-a282-41f6-a7d8-5383ad43cd5b
ms.date: 12/05/2018
ms.keywords: AzAuthorizationStore object [Security],DomainTimeout property, DomainTimeout property [Security], DomainTimeout property [Security],AzAuthorizationStore object, DomainTimeout property [Security],IAzAuthorizationStore interface, IAzAuthorizationStore interface [Security],DomainTimeout property, IAzAuthorizationStore.DomainTimeout, IAzAuthorizationStore.get_DomainTimeout, IAzAuthorizationStore::DomainTimeout, IAzAuthorizationStore::get_DomainTimeout, IAzAuthorizationStore::put_DomainTimeout, azroles/IAzAuthorizationStore::DomainTimeout, azroles/IAzAuthorizationStore::get_DomainTimeout, azroles/IAzAuthorizationStore::put_DomainTimeout, get_DomainTimeout, security.azauthorizationstore_domaintimeout
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzAuthorizationStore::get_DomainTimeout
 - azroles/IAzAuthorizationStore::get_DomainTimeout
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzAuthorizationStore.DomainTimeout
 - IAzAuthorizationStore.get_DomainTimeout
 - IAzAuthorizationStore.put_DomainTimeout
 - AzAuthorizationStore.DomainTimeout
---

# IAzAuthorizationStore::get_DomainTimeout


## -description

The <b>DomainTimeout</b> property sets or retrieves the time in milliseconds after which a domain is determined to be unreachable.

This property is read/write.

## -parameters

## -remarks

After  the specified time-out interval, LDAP query group membership will attempt to contact a domain controller again.

