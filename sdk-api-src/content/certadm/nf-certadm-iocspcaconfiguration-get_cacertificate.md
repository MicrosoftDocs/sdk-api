---
UID: NF:certadm.IOCSPCAConfiguration.get_CACertificate
title: IOCSPCAConfiguration::get_CACertificate (certadm.h)
description: Gets an X.509 certificate that has been encoded by using Distinguished Encoding Rules (DER) and that is for a certification authority (CA).
helpviewer_keywords: ["CACertificate property [Security]","CACertificate property [Security]","IOCSPCAConfiguration interface","IOCSPCAConfiguration interface [Security]","CACertificate property","IOCSPCAConfiguration.CACertificate","IOCSPCAConfiguration.get_CACertificate","IOCSPCAConfiguration::CACertificate","IOCSPCAConfiguration::get_CACertificate","certadm/IOCSPCAConfiguration::CACertificate","certadm/IOCSPCAConfiguration::get_CACertificate","get_CACertificate","security.iocspcaconfiguration_cacertificate_method"]
old-location: security\iocspcaconfiguration_cacertificate_method.htm
tech.root: security
ms.assetid: 73fd56d2-a0d4-4bf8-b818-aadf8cbac9c4
ms.date: 12/05/2018
ms.keywords: CACertificate property [Security], CACertificate property [Security],IOCSPCAConfiguration interface, IOCSPCAConfiguration interface [Security],CACertificate property, IOCSPCAConfiguration.CACertificate, IOCSPCAConfiguration.get_CACertificate, IOCSPCAConfiguration::CACertificate, IOCSPCAConfiguration::get_CACertificate, certadm/IOCSPCAConfiguration::CACertificate, certadm/IOCSPCAConfiguration::get_CACertificate, get_CACertificate, security.iocspcaconfiguration_cacertificate_method
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
 - IOCSPCAConfiguration::get_CACertificate
 - certadm/IOCSPCAConfiguration::get_CACertificate
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
 - IOCSPCAConfiguration.CACertificate
 - IOCSPCAConfiguration.get_CACertificate
---

# IOCSPCAConfiguration::get_CACertificate


## -description

The <b>CACertificate</b> property gets an X.509 certificate that has been encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) and that is for a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA). The default implementations of <a href="/windows/desktop/api/certadm/nn-certadm-iocspadmin">IOCSPAdmin</a> and <a href="/windows/desktop/api/certadm/nn-certadm-iocspcaconfigurationcollection">IOCSPCAConfigurationCollection</a> methods set this value.

This property is read-only.

## -parameters

## -remarks

The <i>pVal</i> certificate corresponds to the certificate used in the <i>varCACert</i> parameter of the <a href="/windows/desktop/api/certadm/nf-certadm-iocspcaconfigurationcollection-createcaconfiguration">CreateCAConfiguration</a> method to create the configuration.

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-iocspadmin">IOCSPCAConfiguration</a>