---
UID: NS:wincrypt._CERT_POLICY_CONSTRAINTS_INFO
title: "_CERT_POLICY_CONSTRAINTS_INFO"
author: windows-sdk-content
description: The CERT_POLICY_CONSTRAINTS_INFO structure contains established policies for accepting certificates as trusted.
old-location: security\cert_policy_constraints_info.htm
tech.root: seccrypto
ms.assetid: f0121ae9-165c-4e86-8672-352a177bb877
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: "*PCERT_POLICY_CONSTRAINTS_INFO, CERT_POLICY_CONSTRAINTS_INFO, CERT_POLICY_CONSTRAINTS_INFO structure [Security], PCERT_POLICY_CONSTRAINTS_INFO, PCERT_POLICY_CONSTRAINTS_INFO structure pointer [Security], _CERT_POLICY_CONSTRAINTS_INFO, _crypto2_cert_policy_constraints_info, security.cert_policy_constraints_info, wincrypt/CERT_POLICY_CONSTRAINTS_INFO, wincrypt/PCERT_POLICY_CONSTRAINTS_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
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
 - Wincrypt.h
api_name:
 - CERT_POLICY_CONSTRAINTS_INFO
product: Windows
targetos: Windows
req.typenames: CERT_POLICY_CONSTRAINTS_INFO, *PCERT_POLICY_CONSTRAINTS_INFO
req.redist: 
---

# _CERT_POLICY_CONSTRAINTS_INFO structure


## -description


The <b>CERT_POLICY_CONSTRAINTS_INFO</b> structure contains established policies for accepting certificates as trusted.


## -struct-fields




### -field fRequireExplicitPolicy

<b>BOOL</b> flag indicating whether explicit policy information is required.


### -field dwRequireExplicitPolicySkipCerts

<b>DWORD</b> indicating the number of required explicit policy certificates.


### -field fInhibitPolicyMapping

<b>BOOL</b> flag indicating whether policy mapping is inhibited.


### -field dwInhibitPolicyMappingSkipCerts

<b>DWORD</b> indicating the number of policy mapping certificates to be skipped.

