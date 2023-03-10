---
UID: NS:ntsecapi._KERB_CERTIFICATE_INFO
title: KERB_CERTIFICATE_INFO (ntsecapi.h)
description: Contains the certificate information.
helpviewer_keywords: ["*PKERB_CERTIFICATE_INFO","KERB_CERTIFICATE_INFO","KERB_CERTIFICATE_INFO structure [Security]","PKERB_CERTIFICATE_INFO","PKERB_CERTIFICATE_INFO structure pointer [Security]","ntsecapi/KERB_CERTIFICATE_INFO","ntsecapi/PKERB_CERTIFICATE_INFO","security.kerb_certificate_info"]
old-location: security\kerb_certificate_info.htm
tech.root: security
ms.assetid: 1E8CA0FE-02DF-4FAA-B0ED-5882DF38B78A
ms.date: 12/05/2018
ms.keywords: '*PKERB_CERTIFICATE_INFO, KERB_CERTIFICATE_INFO, KERB_CERTIFICATE_INFO structure [Security], PKERB_CERTIFICATE_INFO, PKERB_CERTIFICATE_INFO structure pointer [Security], ntsecapi/KERB_CERTIFICATE_INFO, ntsecapi/PKERB_CERTIFICATE_INFO, security.kerb_certificate_info'
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: KERB_CERTIFICATE_INFO, *PKERB_CERTIFICATE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KERB_CERTIFICATE_INFO
 - ntsecapi/_KERB_CERTIFICATE_INFO
 - PKERB_CERTIFICATE_INFO
 - ntsecapi/PKERB_CERTIFICATE_INFO
 - KERB_CERTIFICATE_INFO
 - ntsecapi/KERB_CERTIFICATE_INFO
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
 - KERB_CERTIFICATE_INFO
---

# KERB_CERTIFICATE_INFO structure


## -description

The <b>KERB_CERTIFICATE_INFO</b> structure contains the certificate information.

## -struct-fields

### -field CertInfoSize

The size, in bytes, of the <b>KERB_CERTIFICATE_INFO</b> structure including the marshaled payload which is a structure of type specified in the <i>InfoType</i> parameter and immediately follows the <b>KERB_CERTIFICATE_INFO</b> structure in contiguous memory.

### -field InfoType

A value of the <a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-kerb_certificate_info_type">KERB_CERTIFICATE_INFO_TYPE</a> 	enumeration that specifies the type of certificate information that is provided.