---
UID: NS:wsman._WSMAN_CERTIFICATE_DETAILS
title: WSMAN_CERTIFICATE_DETAILS (wsman.h)
description: Stores client information for an inbound request that was sent with a client certificate.
helpviewer_keywords: ["WSMAN_CERTIFICATE_DETAILS","WSMAN_CERTIFICATE_DETAILS structure [Windows Remote Management]","winrm.wsman_certificate_details","wsman/WSMAN_CERTIFICATE_DETAILS"]
old-location: winrm\wsman_certificate_details.htm
tech.root: winrm
ms.assetid: 82b723fd-c9bb-4ddd-bd2a-4b6d1186846b
ms.date: 12/05/2018
ms.keywords: WSMAN_CERTIFICATE_DETAILS, WSMAN_CERTIFICATE_DETAILS structure [Windows Remote Management], winrm.wsman_certificate_details, wsman/WSMAN_CERTIFICATE_DETAILS
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: WSMAN_CERTIFICATE_DETAILS
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - _WSMAN_CERTIFICATE_DETAILS
 - wsman/_WSMAN_CERTIFICATE_DETAILS
 - WSMAN_CERTIFICATE_DETAILS
 - wsman/WSMAN_CERTIFICATE_DETAILS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsman.h
api_name:
 - WSMAN_CERTIFICATE_DETAILS
---

# WSMAN_CERTIFICATE_DETAILS structure


## -description

Stores client information for an inbound request that was sent with a client certificate.  The individual fields represent the fields within the client certificate.

## -struct-fields

### -field subject

Specifies the subject that is identified by the certificate.

### -field issuerName

Specifies the name of the issuer of the certificate.

### -field issuerThumbprint

Specifies the thumbprint of the issuer.

### -field subjectName

Specifies the subject name of the issuer.

