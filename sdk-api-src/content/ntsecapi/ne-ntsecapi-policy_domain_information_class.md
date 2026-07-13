---
UID: NE:ntsecapi._POLICY_DOMAIN_INFORMATION_CLASS
title: POLICY_DOMAIN_INFORMATION_CLASS (ntsecapi.h)
description: Defines the type of policy domain information.
helpviewer_keywords: ["*PPOLICY_DOMAIN_INFORMATION_CLASS","POLICY_DOMAIN_INFORMATION_CLASS","POLICY_DOMAIN_INFORMATION_CLASS enumeration [Security]","PPOLICY_DOMAIN_INFORMATION_CLASS","PPOLICY_DOMAIN_INFORMATION_CLASS enumeration pointer [Security]","PolicyDomainEfsInformation","PolicyDomainKerberosTicketInformation","ntsecapi/POLICY_DOMAIN_INFORMATION_CLASS","ntsecapi/PPOLICY_DOMAIN_INFORMATION_CLASS","ntsecapi/PolicyDomainEfsInformation","ntsecapi/PolicyDomainKerberosTicketInformation","security.policy_domain_information_class"]
old-location: security\policy_domain_information_class.htm
tech.root: security
ms.assetid: b208c479-a262-4120-824f-677ead1ef61a
ms.date: 12/05/2018
ms.keywords: '*PPOLICY_DOMAIN_INFORMATION_CLASS, POLICY_DOMAIN_INFORMATION_CLASS, POLICY_DOMAIN_INFORMATION_CLASS enumeration [Security], PPOLICY_DOMAIN_INFORMATION_CLASS, PPOLICY_DOMAIN_INFORMATION_CLASS enumeration pointer [Security], PolicyDomainEfsInformation, PolicyDomainKerberosTicketInformation, ntsecapi/POLICY_DOMAIN_INFORMATION_CLASS, ntsecapi/PPOLICY_DOMAIN_INFORMATION_CLASS, ntsecapi/PolicyDomainEfsInformation, ntsecapi/PolicyDomainKerberosTicketInformation, security.policy_domain_information_class'
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
targetos: Windows
req.typenames: POLICY_DOMAIN_INFORMATION_CLASS, *PPOLICY_DOMAIN_INFORMATION_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _POLICY_DOMAIN_INFORMATION_CLASS
 - ntsecapi/_POLICY_DOMAIN_INFORMATION_CLASS
 - PPOLICY_DOMAIN_INFORMATION_CLASS
 - ntsecapi/PPOLICY_DOMAIN_INFORMATION_CLASS
 - POLICY_DOMAIN_INFORMATION_CLASS
 - ntsecapi/POLICY_DOMAIN_INFORMATION_CLASS
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
 - POLICY_DOMAIN_INFORMATION_CLASS
---

# POLICY_DOMAIN_INFORMATION_CLASS enumeration


## -description

The <b>POLICY_DOMAIN_INFORMATION_CLASS</b> enumeration defines the type of policy domain information.

## -enum-fields

### -field PolicyDomainQualityOfServiceInformation:1

### -field PolicyDomainEfsInformation:2

The information is for <a href="/windows/desktop/SecGloss/e-gly">Encrypting File System</a>.

### -field PolicyDomainKerberosTicketInformation

The information is for a Kerberos ticket.
