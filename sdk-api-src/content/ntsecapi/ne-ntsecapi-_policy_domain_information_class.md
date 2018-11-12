---
UID: NE:ntsecapi._POLICY_DOMAIN_INFORMATION_CLASS
title: "_POLICY_DOMAIN_INFORMATION_CLASS"
author: windows-sdk-content
description: Defines the type of policy domain information.
old-location: security\policy_domain_information_class.htm
tech.root: secauthn
ms.assetid: b208c479-a262-4120-824f-677ead1ef61a
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "*PPOLICY_DOMAIN_INFORMATION_CLASS, POLICY_DOMAIN_INFORMATION_CLASS, POLICY_DOMAIN_INFORMATION_CLASS enumeration [Security], PPOLICY_DOMAIN_INFORMATION_CLASS, PPOLICY_DOMAIN_INFORMATION_CLASS enumeration pointer [Security], PolicyDomainEfsInformation, PolicyDomainKerberosTicketInformation, _POLICY_DOMAIN_INFORMATION_CLASS, ntsecapi/POLICY_DOMAIN_INFORMATION_CLASS, ntsecapi/PPOLICY_DOMAIN_INFORMATION_CLASS, ntsecapi/PolicyDomainEfsInformation, ntsecapi/PolicyDomainKerberosTicketInformation, security.policy_domain_information_class"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - POLICY_DOMAIN_INFORMATION_CLASS
product: Windows
targetos: Windows
req.typenames: POLICY_DOMAIN_INFORMATION_CLASS, *PPOLICY_DOMAIN_INFORMATION_CLASS
req.redist: 
---

# _POLICY_DOMAIN_INFORMATION_CLASS enumeration


## -description


The <b>POLICY_DOMAIN_INFORMATION_CLASS</b> enumeration defines the type of policy domain information.


## -enum-fields




### -field PolicyDomainQualityOfServiceInformation


### -field PolicyDomainEfsInformation

The information is for <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">Encrypting File System</a>.


### -field PolicyDomainKerberosTicketInformation

The information is for a Kerberos ticket.

