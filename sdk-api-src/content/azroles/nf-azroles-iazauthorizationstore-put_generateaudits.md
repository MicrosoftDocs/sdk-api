---
UID: NF:azroles.IAzAuthorizationStore.put_GenerateAudits
title: IAzAuthorizationStore::put_GenerateAudits (azroles.h)
description: Sets or retrieves a value that indicates whether run-time audits should be generated. (Put)
helpviewer_keywords: ["AzAuthorizationStore object [Security]","GenerateAudits property","GenerateAudits property [Security]","GenerateAudits property [Security]","AzAuthorizationStore object","GenerateAudits property [Security]","IAzAuthorizationStore interface","IAzAuthorizationStore interface [Security]","GenerateAudits property","IAzAuthorizationStore.GenerateAudits","IAzAuthorizationStore.put_GenerateAudits","IAzAuthorizationStore::GenerateAudits","IAzAuthorizationStore::get_GenerateAudits","IAzAuthorizationStore::put_GenerateAudits","azroles/IAzAuthorizationStore::GenerateAudits","azroles/IAzAuthorizationStore::get_GenerateAudits","azroles/IAzAuthorizationStore::put_GenerateAudits","put_GenerateAudits","security.azauthorizationstore_generateaudits"]
old-location: security\azauthorizationstore_generateaudits.htm
tech.root: security
ms.assetid: e9362ae0-488d-4b6b-9a7b-c70fd85042ca
ms.date: 12/05/2018
ms.keywords: AzAuthorizationStore object [Security],GenerateAudits property, GenerateAudits property [Security], GenerateAudits property [Security],AzAuthorizationStore object, GenerateAudits property [Security],IAzAuthorizationStore interface, IAzAuthorizationStore interface [Security],GenerateAudits property, IAzAuthorizationStore.GenerateAudits, IAzAuthorizationStore.put_GenerateAudits, IAzAuthorizationStore::GenerateAudits, IAzAuthorizationStore::get_GenerateAudits, IAzAuthorizationStore::put_GenerateAudits, azroles/IAzAuthorizationStore::GenerateAudits, azroles/IAzAuthorizationStore::get_GenerateAudits, azroles/IAzAuthorizationStore::put_GenerateAudits, put_GenerateAudits, security.azauthorizationstore_generateaudits
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
 - IAzAuthorizationStore::put_GenerateAudits
 - azroles/IAzAuthorizationStore::put_GenerateAudits
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
 - IAzAuthorizationStore.GenerateAudits
 - IAzAuthorizationStore.get_GenerateAudits
 - IAzAuthorizationStore.put_GenerateAudits
 - AzAuthorizationStore.GenerateAudits
---

# IAzAuthorizationStore::put_GenerateAudits


## -description

The <b>GenerateAudits</b> property sets or retrieves a value that indicates whether run-time audits should be generated.

This property is read/write.

## -parameters

## -remarks

The <b>GenerateAudits</b> property controls application initialization, client context creation, client context deletion,  and access check run-time auditing. The client context can be created by <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID), name, or token.
