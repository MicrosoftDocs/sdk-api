---
UID: NE:ntsecapi._KERB_LOGON_SUBMIT_TYPE
title: "_KERB_LOGON_SUBMIT_TYPE"
author: windows-sdk-content
description: Identifies the type of logon being requested.
old-location: security\kerb_logon_submit_type.htm
old-project: SecAuthN
ms.assetid: 500bee53-638b-4782-b42d-1df158396fb6
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PKERB_LOGON_SUBMIT_TYPE, KERB_LOGON_SUBMIT_TYPE, KERB_LOGON_SUBMIT_TYPE enumeration [Security], KerbCertificateLogon, KerbCertificateS4ULogon, KerbCertificateUnlockLogon, KerbInteractiveLogon, KerbProxyLogon, KerbS4ULogon, KerbSmartCardLogon, KerbSmartCardUnlockLogon, KerbTicketLogon, KerbTicketUnlockLogon, KerbWorkstationUnlockLogon, PKERB_LOGON_SUBMIT_TYPE, PKERB_LOGON_SUBMIT_TYPE enumeration pointer [Security], _KERB_LOGON_SUBMIT_TYPE, _lsa_kerb_logon_submit_type, ntsecapi/KERB_LOGON_SUBMIT_TYPE, ntsecapi/KerbCertificateLogon, ntsecapi/KerbCertificateS4ULogon, ntsecapi/KerbCertificateUnlockLogon, ntsecapi/KerbInteractiveLogon, ntsecapi/KerbProxyLogon, ntsecapi/KerbS4ULogon, ntsecapi/KerbSmartCardLogon, ntsecapi/KerbSmartCardUnlockLogon, ntsecapi/KerbTicketLogon, ntsecapi/KerbTicketUnlockLogon, ntsecapi/KerbWorkstationUnlockLogon, ntsecapi/PKERB_LOGON_SUBMIT_TYPE, security.kerb_logon_submit_type"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: ntsecapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: KERB_LOGON_SUBMIT_TYPE, *PKERB_LOGON_SUBMIT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - KERB_LOGON_SUBMIT_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _KERB_LOGON_SUBMIT_TYPE enumeration


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

Logon using a valid <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">Kerberos</a> ticket as a credential.


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



