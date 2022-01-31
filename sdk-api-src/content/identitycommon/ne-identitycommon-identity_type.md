---
UID: NE:identitycommon._IdentityType
title: IDENTITY_TYPE (identitycommon.h)
description: Specifies the type of identities to enumerate.
helpviewer_keywords: ["IDENTITIES_ALL","IDENTITIES_ME_ONLY","IDENTITY_TYPE","IDENTITY_TYPE enumeration [Security]","identitycommon/IDENTITIES_ALL","identitycommon/IDENTITIES_ME_ONLY","identitycommon/IDENTITY_TYPE","security.identity_type"]
old-location: security\identity_type.htm
tech.root: security
ms.assetid: b15fadf6-5331-4c66-9a6b-0cfdef2ca867
ms.date: 12/05/2018
ms.keywords: IDENTITIES_ALL, IDENTITIES_ME_ONLY, IDENTITY_TYPE, IDENTITY_TYPE enumeration [Security], identitycommon/IDENTITIES_ALL, identitycommon/IDENTITIES_ME_ONLY, identitycommon/IDENTITY_TYPE, security.identity_type
req.header: identitycommon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: IDENTITY_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IdentityType
 - identitycommon/_IdentityType
 - IDENTITY_TYPE
 - identitycommon/IDENTITY_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Identitycommon.h
api_name:
 - IDENTITY_TYPE
---

# IDENTITY_TYPE enumeration


## -description

Specifies the type of identities to enumerate. This enumeration is used by the <a href="/windows/desktop/api/identityprovider/nf-identityprovider-iidentityprovider-getidentityenum">IIdentityProvider::GetIdentityEnum</a> and <a href="/windows/desktop/api/identitystore/nf-identitystore-iidentitystore-enumerateidentities">IIdentityStore::EnumerateIdentities</a> methods.

## -enum-fields

### -field IDENTITIES_ALL:0

Enumerate all identities.

### -field IDENTITIES_ME_ONLY:0x1

Enumerate only identities associated with the current user.
