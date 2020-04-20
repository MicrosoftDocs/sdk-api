---
UID: NE:ntsecapi._KERB_LOGON_SUBMIT_TYPE
title: KERB_LOGON_SUBMIT_TYPE (ntsecapi.h)
description: Identifies the type of logon being requested.helpviewer_keywords: ["*PKERB_LOGON_SUBMIT_TYPE","KERB_LOGON_SUBMIT_TYPE","KERB_LOGON_SUBMIT_TYPE enumeration [Security]","KerbCertificateLogon","KerbCertificateS4ULogon","KerbCertificateUnlockLogon","KerbInteractiveLogon","KerbProxyLogon","KerbS4ULogon","KerbSmartCardLogon","KerbSmartCardUnlockLogon","KerbTicketLogon","KerbTicketUnlockLogon","KerbWorkstationUnlockLogon","PKERB_LOGON_SUBMIT_TYPE","PKERB_LOGON_SUBMIT_TYPE enumeration pointer [Security]","_lsa_kerb_logon_submit_type","ntsecapi/KERB_LOGON_SUBMIT_TYPE","ntsecapi/KerbCertificateLogon","ntsecapi/KerbCertificateS4ULogon","ntsecapi/KerbCertificateUnlockLogon","ntsecapi/KerbInteractiveLogon","ntsecapi/KerbProxyLogon","ntsecapi/KerbS4ULogon","ntsecapi/KerbSmartCardLogon","ntsecapi/KerbSmartCardUnlockLogon","ntsecapi/KerbTicketLogon","ntsecapi/KerbTicketUnlockLogon","ntsecapi/KerbWorkstationUnlockLogon","ntsecapi/PKERB_LOGON_SUBMIT_TYPE","security.kerb_logon_submit_type"]
old-location: security\kerb_logon_submit_type.htm
tech.root: SecAuthN
ms.assetid: 500bee53-638b-4782-b42d-1df158396fb6
ms.date: 12/05/2018
ms.keywords: '*PKERB_LOGON_SUBMIT_TYPE, KERB_LOGON_SUBMIT_TYPE, KERB_LOGON_SUBMIT_TYPE enumeration [Security], KerbCertificateLogon, KerbCertificateS4ULogon, KerbCertificateUnlockLogon, KerbInteractiveLogon, KerbProxyLogon, KerbS4ULogon, KerbSmartCardLogon, KerbSmartCardUnlockLogon, KerbTicketLogon, KerbTicketUnlockLogon, KerbWorkstationUnlockLogon, PKERB_LOGON_SUBMIT_TYPE, PKERB_LOGON_SUBMIT_TYPE enumeration pointer [Security], _lsa_kerb_logon_submit_type, ntsecapi/KERB_LOGON_SUBMIT_TYPE, ntsecapi/KerbCertificateLogon, ntsecapi/KerbCertificateS4ULogon, ntsecapi/KerbCertificateUnlockLogon, ntsecapi/KerbInteractiveLogon, ntsecapi/KerbProxyLogon, ntsecapi/KerbS4ULogon, ntsecapi/KerbSmartCardLogon, ntsecapi/KerbSmartCardUnlockLogon, ntsecapi/KerbTicketLogon, ntsecapi/KerbTicketUnlockLogon, ntsecapi/KerbWorkstationUnlockLogon, ntsecapi/PKERB_LOGON_SUBMIT_TYPE, security.kerb_logon_submit_type'
f1_keywords:
- ntsecapi/KERB_LOGON_SUBMIT_TYPE
dev_langs:
- c++
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Ntsecapi.h
api_name:
- KERB_LOGON_SUBMIT_TYPE
targetos: Windows
req.typenames: KERB_LOGON_SUBMIT_TYPE, *PKERB_LOGON_SUBMIT_TYPE
req.redist: 
ms.custom: 19H1
---

# KERB_LOGON_SUBMIT_TYPE enumeration


## -description


The <b>KERB_LOGON_SUBMIT_TYPE</b> enumeration identifies the type of logon being requested.


## -enum-fields




### -field KerbInteractiveLogon

Perform an interactive logon.


### -field KerbSmartCardLogon

Logon using a smart card.


### -field KerbWorkstationUnlockLogon

Unlock a workstation.


### -field KerbSmartCardUnlockLogon

Unlock a workstation using a smart card.


### -field KerbProxyLogon

Logon using a proxy server.


### -field KerbTicketLogon

Logon using a valid <a href="https://docs.microsoft.com/windows/desktop/SecGloss/k-gly">Kerberos</a> ticket as a credential.


### -field KerbTicketUnlockLogon

Unlock a workstation by using a Kerberos ticket.


### -field KerbS4ULogon

Perform a service for user logon.


### -field KerbCertificateLogon

Logon interactively using a certificate stored on a smart card.


### -field KerbCertificateS4ULogon

Perform a service for user logon using a certificate stored on a smart card.


### -field KerbCertificateUnlockLogon

Unlock a workstation using a certificate stored on a smart card.


### -field KerbNoElevationLogon


### -field KerbLuidLogon



