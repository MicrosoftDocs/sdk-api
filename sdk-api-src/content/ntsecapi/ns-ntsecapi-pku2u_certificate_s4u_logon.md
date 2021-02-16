---
UID: NS:ntsecapi._PKU2U_CERTIFICATE_S4U_LOGON
title: PKU2U_CERTIFICATE_S4U_LOGON (ntsecapi.h)
description: Specifies a certificate used for S4U logon.
helpviewer_keywords: ["*PPKU2U_CERTIFICATE_S4U_LOGON","PKU2U_CERTIFICATE_S4U_LOGON","PKU2U_CERTIFICATE_S4U_LOGON structure [Security]","PPKU2U_CERTIFICATE_S4U_LOGON","PPKU2U_CERTIFICATE_S4U_LOGON structure pointer [Security]","ntsecapi/PKU2U_CERTIFICATE_S4U_LOGON","ntsecapi/PPKU2U_CERTIFICATE_S4U_LOGON","security.pku2u_certificate_s4u_logon"]
old-location: security\pku2u_certificate_s4u_logon.htm
tech.root: security
ms.assetid: 438b5637-d711-419a-a163-a9b014bf0662
ms.date: 12/05/2018
ms.keywords: '*PPKU2U_CERTIFICATE_S4U_LOGON, PKU2U_CERTIFICATE_S4U_LOGON, PKU2U_CERTIFICATE_S4U_LOGON structure [Security], PPKU2U_CERTIFICATE_S4U_LOGON, PPKU2U_CERTIFICATE_S4U_LOGON structure pointer [Security], ntsecapi/PKU2U_CERTIFICATE_S4U_LOGON, ntsecapi/PPKU2U_CERTIFICATE_S4U_LOGON, security.pku2u_certificate_s4u_logon'
req.header: ntsecapi.h
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
req.typenames: PKU2U_CERTIFICATE_S4U_LOGON, *PPKU2U_CERTIFICATE_S4U_LOGON
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PKU2U_CERTIFICATE_S4U_LOGON
 - ntsecapi/_PKU2U_CERTIFICATE_S4U_LOGON
 - PPKU2U_CERTIFICATE_S4U_LOGON
 - ntsecapi/PPKU2U_CERTIFICATE_S4U_LOGON
 - PKU2U_CERTIFICATE_S4U_LOGON
 - ntsecapi/PKU2U_CERTIFICATE_S4U_LOGON
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
 - PKU2U_CERTIFICATE_S4U_LOGON
---

# PKU2U_CERTIFICATE_S4U_LOGON structure


## -description

Specifies a certificate used for S4U logon.

## -struct-fields

### -field MessageType

A value of the <a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-pku2u_logon_submit_type">PKU2U_LOGON_SUBMIT_TYPE</a> enumeration that indicates the logon type.

### -field Flags

This member is reserved. Do not use it.

### -field UserPrincipalName

The name of the user who is attempting to authenticate.

### -field DomainName

This member is reserved. Do not use it.

### -field CertificateLength

The size, in bytes, of the <b>Certificate</b> buffer.

### -field Certificate

The certificate data.

