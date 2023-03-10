---
UID: NE:sspi._SECPKG_CRED_CLASS
title: SECPKG_CRED_CLASS (sspi.h)
description: Indicates the type of credential used in a client context. The SECPKG_CRED_CLASS enumeration is used in the SecPkgContext_CredInfo structure.
helpviewer_keywords: ["*PSECPKG_CRED_CLASS","PSECPKG_CRED_CLASS","PSECPKG_CRED_CLASS enumeration pointer [Security]","SECPKG_CRED_CLASS","SECPKG_CRED_CLASS enumeration [Security]","SecPkgCredClass_Ephemeral","SecPkgCredClass_Explicit = 40","SecPkgCredClass_None","SecPkgCredClass_PersistedGeneric","SecPkgCredClass_PersistedSpecific","security.secpkg_cred_class","sspi/PSECPKG_CRED_CLASS","sspi/SECPKG_CRED_CLASS","sspi/SecPkgCredClass_Ephemeral","sspi/SecPkgCredClass_Explicit = 40","sspi/SecPkgCredClass_None","sspi/SecPkgCredClass_PersistedGeneric","sspi/SecPkgCredClass_PersistedSpecific"]
old-location: security\secpkg_cred_class.htm
tech.root: security
ms.assetid: 2f5f9be2-e7b5-4d34-a2ad-89a99db78ad0
ms.date: 12/05/2018
ms.keywords: '*PSECPKG_CRED_CLASS, PSECPKG_CRED_CLASS, PSECPKG_CRED_CLASS enumeration pointer [Security], SECPKG_CRED_CLASS, SECPKG_CRED_CLASS enumeration [Security], SecPkgCredClass_Ephemeral, SecPkgCredClass_Explicit = 40, SecPkgCredClass_None, SecPkgCredClass_PersistedGeneric, SecPkgCredClass_PersistedSpecific, security.secpkg_cred_class, sspi/PSECPKG_CRED_CLASS, sspi/SECPKG_CRED_CLASS, sspi/SecPkgCredClass_Ephemeral, sspi/SecPkgCredClass_Explicit = 40, sspi/SecPkgCredClass_None, sspi/SecPkgCredClass_PersistedGeneric, sspi/SecPkgCredClass_PersistedSpecific'
req.header: sspi.h
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
req.typenames: SECPKG_CRED_CLASS, *PSECPKG_CRED_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECPKG_CRED_CLASS
 - sspi/_SECPKG_CRED_CLASS
 - PSECPKG_CRED_CLASS
 - sspi/PSECPKG_CRED_CLASS
 - SECPKG_CRED_CLASS
 - sspi/SECPKG_CRED_CLASS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SECPKG_CRED_CLASS
---

# SECPKG_CRED_CLASS enumeration


## -description

Indicates the type of credential used in a client context. The <b>SECPKG_CRED_CLASS</b> enumeration is used in the <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_credinfo">SecPkgContext_CredInfo</a> structure.

## -enum-fields

### -field SecPkgCredClass_None:0

No credentials are supplied.

### -field SecPkgCredClass_Ephemeral:10

Indicates the credentials used to log on to the system.

### -field SecPkgCredClass_PersistedGeneric:20

Indicates saved credentials that are not target specific.

### -field SecPkgCredClass_PersistedSpecific:30

Indicates saved credentials that are target specific.

### -field SecPkgCredClass_Explicit = 40

Indicates credentials explicitly supplied by the user.
