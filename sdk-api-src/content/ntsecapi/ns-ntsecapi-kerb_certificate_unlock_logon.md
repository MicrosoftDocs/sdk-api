---
UID: NS:ntsecapi._KERB_CERTIFICATE_UNLOCK_LOGON
title: KERB_CERTIFICATE_UNLOCK_LOGON (ntsecapi.h)
author: windows-sdk-content
description: Contains information used to unlock a workstation that has been locked during an interactive smart card logon session.
old-location: security\kerb_certificate_unlock_logon.htm
tech.root: SecAuthN
ms.assetid: 04e058b0-9a05-4ed7-9d4a-1c8c003d8077
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PKERB_CERTIFICATE_UNLOCK_LOGON, KERB_CERTIFICATE_UNLOCK_LOGON, KERB_CERTIFICATE_UNLOCK_LOGON structure [Security], PKERB_CERTIFICATE_UNLOCK_LOGON, PKERB_CERTIFICATE_UNLOCK_LOGON structure pointer [Security], ntsecapi/KERB_CERTIFICATE_UNLOCK_LOGON, ntsecapi/PKERB_CERTIFICATE_UNLOCK_LOGON, security.kerb_certificate_unlock_logon'
ms.topic: struct
f1_keywords:
- ntsecapi/KERB_CERTIFICATE_UNLOCK_LOGON
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
- KERB_CERTIFICATE_UNLOCK_LOGON
product: Windows
targetos: Windows
req.typenames: KERB_CERTIFICATE_UNLOCK_LOGON, *PKERB_CERTIFICATE_UNLOCK_LOGON
req.redist: 
ms.custom: 19H1
---

# KERB_CERTIFICATE_UNLOCK_LOGON structure


## -description


The <b>KERB_CERTIFICATE_UNLOCK_LOGON</b> structure contains information used to unlock a workstation that has been locked during an interactive smart card <a href="https://docs.microsoft.com/windows/desktop/SecGloss/l-gly">logon session</a>.

It is passed as the <i>AuthenticationInformation</i> parameter to the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a> function when using the <a href="https://docs.microsoft.com/windows/desktop/SecAuthN/kerberos-ssp-ap">Kerberos</a> security package to unlock a logon session.


## -struct-fields




### -field Logon

A <a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_certificate_logon">KERB_CERTIFICATE_LOGON</a> structure that contains information about the logon session to unlock.

The <b>MessageType</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_certificate_logon">KERB_CERTIFICATE_LOGON</a> structure must be set to <b>KerbCertificateUnlockLogon</b>.


### -field LogonId

A <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-luid">LUID</a> structure that identifies the logon session to unlock. This member is set by <a href="https://docs.microsoft.com/windows/desktop/SecAuthN/winlogon">Winlogon</a>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_certificate_logon">KERB_CERTIFICATE_LOGON</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthN/kerb-smartcard-csp-info">KERB_SMARTCARD_CSP_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a>
 

 

