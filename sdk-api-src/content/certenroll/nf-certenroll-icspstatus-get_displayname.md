---
UID: NF:certenroll.ICspStatus.get_DisplayName
title: ICspStatus::get_DisplayName (certenroll.h)
description: Retrieves a string that contains the name of the provider, the algorithm name, and the operations that can be performed by the algorithm.
helpviewer_keywords: ["DisplayName property [Security]","DisplayName property [Security]","ICspStatus interface","ICspStatus interface [Security]","DisplayName property","ICspStatus.DisplayName","ICspStatus.get_DisplayName","ICspStatus::DisplayName","ICspStatus::get_DisplayName","certenroll/ICspStatus::DisplayName","certenroll/ICspStatus::get_DisplayName","get_DisplayName","security.icspstatus_displayname"]
old-location: security\icspstatus_displayname.htm
tech.root: security
ms.assetid: 7c778f78-1e94-4e84-a51a-3c0171f19db6
ms.date: 12/05/2018
ms.keywords: DisplayName property [Security], DisplayName property [Security],ICspStatus interface, ICspStatus interface [Security],DisplayName property, ICspStatus.DisplayName, ICspStatus.get_DisplayName, ICspStatus::DisplayName, ICspStatus::get_DisplayName, certenroll/ICspStatus::DisplayName, certenroll/ICspStatus::get_DisplayName, get_DisplayName, security.icspstatus_displayname
req.header: certenroll.h
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
req.dll: CertEnroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICspStatus::get_DisplayName
 - certenroll/ICspStatus::get_DisplayName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICspStatus.DisplayName
 - ICspStatus.get_DisplayName
---

# ICspStatus::get_DisplayName


## -description

The <b>DisplayName</b> property retrieves a string that contains the name of the provider, the algorithm name, and the operations that can be performed by the algorithm.

This property is read-only.

## -parameters

## -remarks

The format of the string returned by this property depends on whether the provider is a CryptoAPI <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) or a Cryptography API: Next Generation (CNG) provider.<ul>
<li>The format of the string for a CSP is <i>ProviderName(KeyType)</i> where <i>KeyType</i> is either "Signature" or "Encryption".</li>
<li>The format of the string for a CNG provider is <i>AlgorithmName,ProviderName</i> where <i>AlgorithmName</i> can be "Unknown Algorithm".</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatuses">ICspStatuses</a>