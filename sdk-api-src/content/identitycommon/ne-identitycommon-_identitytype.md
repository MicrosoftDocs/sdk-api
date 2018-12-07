---
UID: NE:identitycommon._IdentityType
title: "_IdentityType"
author: windows-sdk-content
description: Specifies the type of identities to enumerate.
old-location: security\identity_type.htm
tech.root: secauthn
ms.assetid: b15fadf6-5331-4c66-9a6b-0cfdef2ca867
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDENTITIES_ALL, IDENTITIES_ME_ONLY, IDENTITY_TYPE, IDENTITY_TYPE enumeration [Security], _IdentityType, identitycommon/IDENTITIES_ALL, identitycommon/IDENTITIES_ME_ONLY, identitycommon/IDENTITY_TYPE, security.identity_type
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Identitycommon.h
api_name:
 - IDENTITY_TYPE
product: Windows
targetos: Windows
req.typenames: IDENTITY_TYPE
req.redist: 
---

# _IdentityType enumeration


## -description


Specifies the type of identities to enumerate. This enumeration is used by the <a href="https://msdn.microsoft.com/9e216959-7038-43cf-a57d-bee85d521f58">IIdentityProvider::GetIdentityEnum</a> and <a href="https://msdn.microsoft.com/df1a53e0-6296-49ed-b0f0-85e9dc9ab947">IIdentityStore::EnumerateIdentities</a> methods.


## -enum-fields




### -field IDENTITIES_ALL

Enumerate all identities.


### -field IDENTITIES_ME_ONLY

Enumerate only identities associated with the current user.

