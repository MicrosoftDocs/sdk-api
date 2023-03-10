---
UID: NF:certadm.IOCSPCAConfiguration.get_LocalRevocationInformation
title: IOCSPCAConfiguration::get_LocalRevocationInformation (certadm.h)
description: Gets or sets the certificate revocation list (CRL) of the local machine. (Get)
helpviewer_keywords: ["IOCSPCAConfiguration interface [Security]","LocalRevocationInformation property","IOCSPCAConfiguration.LocalRevocationInformation","IOCSPCAConfiguration.get_LocalRevocationInformation","IOCSPCAConfiguration::LocalRevocationInformation","IOCSPCAConfiguration::get_LocalRevocationInformation","IOCSPCAConfiguration::put_LocalRevocationInformation","LocalRevocationInformation property [Security]","LocalRevocationInformation property [Security]","IOCSPCAConfiguration interface","certadm/IOCSPCAConfiguration::LocalRevocationInformation","certadm/IOCSPCAConfiguration::get_LocalRevocationInformation","certadm/IOCSPCAConfiguration::put_LocalRevocationInformation","get_LocalRevocationInformation","security.iocspcaconfiguration_localrevocationinformation"]
old-location: security\iocspcaconfiguration_localrevocationinformation.htm
tech.root: security
ms.assetid: 76581c1c-9eba-456c-b1cb-ff61e530a53a
ms.date: 12/05/2018
ms.keywords: IOCSPCAConfiguration interface [Security],LocalRevocationInformation property, IOCSPCAConfiguration.LocalRevocationInformation, IOCSPCAConfiguration.get_LocalRevocationInformation, IOCSPCAConfiguration::LocalRevocationInformation, IOCSPCAConfiguration::get_LocalRevocationInformation, IOCSPCAConfiguration::put_LocalRevocationInformation, LocalRevocationInformation property [Security], LocalRevocationInformation property [Security],IOCSPCAConfiguration interface, certadm/IOCSPCAConfiguration::LocalRevocationInformation, certadm/IOCSPCAConfiguration::get_LocalRevocationInformation, certadm/IOCSPCAConfiguration::put_LocalRevocationInformation, get_LocalRevocationInformation, security.iocspcaconfiguration_localrevocationinformation
req.header: certadm.h
req.include-header: Certserv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certadm.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOCSPCAConfiguration::get_LocalRevocationInformation
 - certadm/IOCSPCAConfiguration::get_LocalRevocationInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IOCSPCAConfiguration.LocalRevocationInformation
 - IOCSPCAConfiguration.get_LocalRevocationInformation
 - IOCSPCAConfiguration.put_LocalRevocationInformation
---

# IOCSPCAConfiguration::get_LocalRevocationInformation


## -description

 The <b>LocalRevocationInformation</b> property gets or sets the <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) of the local machine. This list provides additional revocation information, or supersedes information from the revocation provider configured by <a href="/windows/desktop/api/certadm/nf-certadm-iocspcaconfiguration-get_providerclsid">ProviderCLSID</a>.

This property is read/write.

## -parameters

## -remarks

The CRL used for the <b>LocalRevocationInformation</b> property can be signed or not signed. There is no signature verification for the CRL.

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-iocspcaconfiguration">IOCSPCAConfiguration</a>
