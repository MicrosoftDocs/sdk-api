---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

