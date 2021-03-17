---
UID: NF:certadm.IOCSPCAConfiguration.get_CSPName
title: IOCSPCAConfiguration::get_CSPName (certadm.h)
description: Gets a cryptographic service provider (CSP) or key storage provider (KSP) name.
helpviewer_keywords: ["CSPName property [Security]","CSPName property [Security]","IOCSPCAConfiguration interface","IOCSPCAConfiguration interface [Security]","CSPName property","IOCSPCAConfiguration.CSPName","IOCSPCAConfiguration.get_CSPName","IOCSPCAConfiguration::CSPName","IOCSPCAConfiguration::get_CSPName","certadm/IOCSPCAConfiguration::CSPName","certadm/IOCSPCAConfiguration::get_CSPName","get_CSPName","security.iocspcaconfiguration_cspname_method"]
old-location: security\iocspcaconfiguration_cspname_method.htm
tech.root: security
ms.assetid: a35400a9-7eb7-4298-b023-efe2a087ba7d
ms.date: 12/05/2018
ms.keywords: CSPName property [Security], CSPName property [Security],IOCSPCAConfiguration interface, IOCSPCAConfiguration interface [Security],CSPName property, IOCSPCAConfiguration.CSPName, IOCSPCAConfiguration.get_CSPName, IOCSPCAConfiguration::CSPName, IOCSPCAConfiguration::get_CSPName, certadm/IOCSPCAConfiguration::CSPName, certadm/IOCSPCAConfiguration::get_CSPName, get_CSPName, security.iocspcaconfiguration_cspname_method
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
 - IOCSPCAConfiguration::get_CSPName
 - certadm/IOCSPCAConfiguration::get_CSPName
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
 - IOCSPCAConfiguration.CSPName
 - IOCSPCAConfiguration.get_CSPName
---

# IOCSPCAConfiguration::get_CSPName


## -description

The <b>CSPName</b> property gets a <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) or <a href="/windows/desktop/SecGloss/k-gly">key storage provider</a> (KSP) name. The default implementations of <a href="/windows/desktop/api/certadm/nn-certadm-iocspadmin">IOCSPAdmin</a> and <a href="/windows/desktop/api/certadm/nn-certadm-iocspcaconfigurationcollection">IOCSPCAConfigurationCollection</a> set this value.

This property is read-only.

## -parameters

## -remarks

The name returned in <i>pVal</i> corresponds to the CSP or KSP used for the <a href="/windows/desktop/api/certadm/nf-certadm-iocspcaconfiguration-get_signingcertificate">SigningCertificate</a> property.

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-iocspcaconfiguration">IOCSPCAConfiguration</a>