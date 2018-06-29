---
UID: NS:ntsecapi._KERB_CERTIFICATE_UNLOCK_LOGON
title: "_KERB_CERTIFICATE_UNLOCK_LOGON"
author: windows-sdk-content
description: Contains information used to unlock a workstation that has been locked during an interactive smart card logon session.
old-location: security\kerb_certificate_unlock_logon.htm
old-project: SecAuthN
ms.assetid: 04e058b0-9a05-4ed7-9d4a-1c8c003d8077
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PKERB_CERTIFICATE_UNLOCK_LOGON, KERB_CERTIFICATE_UNLOCK_LOGON, KERB_CERTIFICATE_UNLOCK_LOGON structure [Security], PKERB_CERTIFICATE_UNLOCK_LOGON, PKERB_CERTIFICATE_UNLOCK_LOGON structure pointer [Security], _KERB_CERTIFICATE_UNLOCK_LOGON, ntsecapi/KERB_CERTIFICATE_UNLOCK_LOGON, ntsecapi/PKERB_CERTIFICATE_UNLOCK_LOGON, security.kerb_certificate_unlock_logon"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: KERB_CERTIFICATE_UNLOCK_LOGON, *PKERB_CERTIFICATE_UNLOCK_LOGON
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
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _KERB_CERTIFICATE_UNLOCK_LOGON structure


## -description


The <b>KERB_CERTIFICATE_UNLOCK_LOGON</b> structure contains information used to unlock a workstation that has been locked during an interactive smart card <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon session</a>.

It is passed as the <i>AuthenticationInformation</i> parameter to the 
<a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a> function when using the <a href="https://msdn.microsoft.com/43970c99-53f1-43c1-9d9f-65573572f731">Kerberos</a> security package to unlock a logon session.


## -struct-fields




### -field Logon

A <a href="https://msdn.microsoft.com/e6aa0042-edb5-4e9b-b545-5159d3bfb8fc">KERB_CERTIFICATE_LOGON</a> structure that contains information about the logon session to unlock.

The <b>MessageType</b> member of the <a href="https://msdn.microsoft.com/e6aa0042-edb5-4e9b-b545-5159d3bfb8fc">KERB_CERTIFICATE_LOGON</a> structure must be set to <b>KerbCertificateUnlockLogon</b>.


### -field LogonId

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a> structure that identifies the logon session to unlock. This member is set by <a href="https://msdn.microsoft.com/library/windows/hardware/dn927313">Winlogon</a>.


## -see-also




<a href="https://msdn.microsoft.com/e6aa0042-edb5-4e9b-b545-5159d3bfb8fc">KERB_CERTIFICATE_LOGON</a>



<a href="https://msdn.microsoft.com/b3e6722a-25dd-4137-b224-4082e846ddec">KERB_SMARTCARD_CSP_INFO</a>



<a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a>
 

 

