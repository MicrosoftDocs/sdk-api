---
UID: NE:sspi._SEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS
title: SEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS (sspi.h)
description: Describes the status of the SEC application protocol negotiation.
helpviewer_keywords: ["*PSEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS","PSEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS","PSEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS enumeration pointer [Security]","SEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS","SEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS enumeration [Security]","SecApplicationProtocolNegotiationStatus_None","SecApplicationProtocolNegotiationStatus_SelectedClientOnly","SecApplicationProtocolNegotiationStatus_Success","security.sec_application_protocol_negotiation_status","sspi/PSEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS","sspi/SEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS","sspi/SecApplicationProtocolNegotiationStatus_None","sspi/SecApplicationProtocolNegotiationStatus_SelectedClientOnly","sspi/SecApplicationProtocolNegotiationStatus_Success"]
old-location: security\sec_application_protocol_negotiation_status.htm
tech.root: security
ms.assetid: 64236EA6-C0CE-484A-9B12-4E653790D281
ms.date: 12/05/2018
ms.keywords: '*PSEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS, PSEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS, PSEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS enumeration pointer [Security], SEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS, SEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS enumeration [Security], SecApplicationProtocolNegotiationStatus_None, SecApplicationProtocolNegotiationStatus_SelectedClientOnly, SecApplicationProtocolNegotiationStatus_Success, security.sec_application_protocol_negotiation_status, sspi/PSEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS, sspi/SEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS, sspi/SecApplicationProtocolNegotiationStatus_None, sspi/SecApplicationProtocolNegotiationStatus_SelectedClientOnly, sspi/SecApplicationProtocolNegotiationStatus_Success'
req.header: sspi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.typenames: SEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS, *PSEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS
 - sspi/_SEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS
 - PSEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS
 - sspi/PSEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS
 - SEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS
 - sspi/SEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS
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
 - SEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS
---

# SEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS enumeration

## -description

Describes the status of the SEC application protocol negotiation.

## -enum-fields

### -field SecApplicationProtocolNegotiationStatus_None

No application protocol was negotiated.

### -field SecApplicationProtocolNegotiationStatus_Success

The application protocol was negotiated successfully.

### -field SecApplicationProtocolNegotiationStatus_SelectedClientOnly

The application protocol was negotiated successfully, but for selected clients only.
