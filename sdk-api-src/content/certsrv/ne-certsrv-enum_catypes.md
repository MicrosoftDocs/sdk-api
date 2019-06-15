---
UID: NE:certsrv.__unnamed_enum_0
title: ENUM_CATYPES (certsrv.h)
author: windows-sdk-content
description: Specifies a certification authority (CA) type.
old-location: security\enum_catypes.htm
tech.root: SecCrypto
ms.assetid: 32b20317-c0ef-4896-a8c6-309e34f87c30
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ENUM_CATYPES, ENUM_CATYPES enumeration [Security], ENUM_ENTERPRISE_ROOTCA, ENUM_ENTERPRISE_SUBCA, ENUM_STANDALONE_ROOTCA, ENUM_STANDALONE_SUBCA, ENUM_UNKNOWN_CA, certsrv/ENUM_CATYPES, certsrv/ENUM_ENTERPRISE_ROOTCA, certsrv/ENUM_ENTERPRISE_SUBCA, certsrv/ENUM_STANDALONE_ROOTCA, certsrv/ENUM_STANDALONE_SUBCA, certsrv/ENUM_UNKNOWN_CA, security.enum_catypes
ms.topic: enum
f1_keywords: ["certsrv/ENUM_CATYPES"]
req.header: certsrv.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Certsrv.h
api_name:
 - ENUM_CATYPES
product: Windows
targetos: Windows
req.typenames: ENUM_CATYPES
req.redist: 
ms.custom: 19H1
---

# ENUM_CATYPES enumeration


## -description


The <b>ENUM_CATYPES</b> enumeration specifies a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) type.


## -enum-fields




### -field ENUM_ENTERPRISE_ROOTCA

A root CA that is a member of an Active Directory domain and uses Directory Service to issue and manage certificates.


### -field ENUM_ENTERPRISE_SUBCA

A CA  that uses Directory Service to issue and manage certificates and is subordinate to an enterprise root CA.


### -field ENUM_STANDALONE_ROOTCA

A root CA that does not use Directory Service to issue or manage certificates. It might or might not belong to a domain.


### -field ENUM_STANDALONE_SUBCA

A CA that does not use Directory Service to issue or manage certificates and is subordinate to a standalone root CA.


### -field ENUM_UNKNOWN_CA

An unknown CA type.

