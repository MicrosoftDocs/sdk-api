---
UID: NE:iketypes.IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE_
title: IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE (iketypes.h)
description: Specifies the type of impersonation to perform when Authenticated Internet Protocol (AuthIP) is used for authentication.
helpviewer_keywords: ["IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE","IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE enumeration [Filtering]","IKEEXT_IMPERSONATION_MAX","IKEEXT_IMPERSONATION_NONE","IKEEXT_IMPERSONATION_SOCKET_PRINCIPAL","fwp.ikeext_authentication_impersonation_type","iketypes/IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE","iketypes/IKEEXT_IMPERSONATION_MAX","iketypes/IKEEXT_IMPERSONATION_NONE","iketypes/IKEEXT_IMPERSONATION_SOCKET_PRINCIPAL"]
old-location: fwp\ikeext_authentication_impersonation_type.htm
tech.root: fwp
ms.assetid: 840c7429-5a1a-4e3f-823c-c46a412cbe71
ms.date: 12/05/2018
ms.keywords: IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE, IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE enumeration [Filtering], IKEEXT_IMPERSONATION_MAX, IKEEXT_IMPERSONATION_NONE, IKEEXT_IMPERSONATION_SOCKET_PRINCIPAL, fwp.ikeext_authentication_impersonation_type, iketypes/IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE, iketypes/IKEEXT_IMPERSONATION_MAX, iketypes/IKEEXT_IMPERSONATION_NONE, iketypes/IKEEXT_IMPERSONATION_SOCKET_PRINCIPAL
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE_
 - iketypes/IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE_
 - IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE
 - iketypes/IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE
---

# IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE enumeration


## -description

The <b>IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE</b> enumerated type specifies the type of impersonation to perform when Authenticated Internet Protocol (AuthIP) is used for authentication.

## -enum-fields

### -field IKEEXT_IMPERSONATION_NONE:0

Specifies no impersonation.

### -field IKEEXT_IMPERSONATION_SOCKET_PRINCIPAL

Specifies socket principal impersonation.

### -field IKEEXT_IMPERSONATION_MAX

Maximum value for testing purposes.

## -see-also

<a href="/windows/desktop/FWP/fwp-enums">Windows Filtering Platform API Enumerated Types</a>
