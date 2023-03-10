---
UID: NF:certadm.IOCSPCAConfiguration.get_SigningCertificateTemplate
title: IOCSPCAConfiguration::get_SigningCertificateTemplate (certadm.h)
description: Gets or sets the template name for a signing certificate. (Get)
helpviewer_keywords: ["IOCSPCAConfiguration interface [Security]","SigningCertificateTemplate property","IOCSPCAConfiguration.SigningCertificateTemplate","IOCSPCAConfiguration.get_SigningCertificateTemplate","IOCSPCAConfiguration::SigningCertificateTemplate","IOCSPCAConfiguration::get_SigningCertificateTemplate","IOCSPCAConfiguration::put_SigningCertificateTemplate","SigningCertificateTemplate property [Security]","SigningCertificateTemplate property [Security]","IOCSPCAConfiguration interface","certadm/IOCSPCAConfiguration::SigningCertificateTemplate","certadm/IOCSPCAConfiguration::get_SigningCertificateTemplate","certadm/IOCSPCAConfiguration::put_SigningCertificateTemplate","get_SigningCertificateTemplate","security.iocspcaconfiguration_signingcertificatetemplate"]
old-location: security\iocspcaconfiguration_signingcertificatetemplate.htm
tech.root: security
ms.assetid: 38e75d8f-1e6a-4214-8142-85f7e9c41ce2
ms.date: 12/05/2018
ms.keywords: IOCSPCAConfiguration interface [Security],SigningCertificateTemplate property, IOCSPCAConfiguration.SigningCertificateTemplate, IOCSPCAConfiguration.get_SigningCertificateTemplate, IOCSPCAConfiguration::SigningCertificateTemplate, IOCSPCAConfiguration::get_SigningCertificateTemplate, IOCSPCAConfiguration::put_SigningCertificateTemplate, SigningCertificateTemplate property [Security], SigningCertificateTemplate property [Security],IOCSPCAConfiguration interface, certadm/IOCSPCAConfiguration::SigningCertificateTemplate, certadm/IOCSPCAConfiguration::get_SigningCertificateTemplate, certadm/IOCSPCAConfiguration::put_SigningCertificateTemplate, get_SigningCertificateTemplate, security.iocspcaconfiguration_signingcertificatetemplate
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
 - IOCSPCAConfiguration::get_SigningCertificateTemplate
 - certadm/IOCSPCAConfiguration::get_SigningCertificateTemplate
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
 - IOCSPCAConfiguration.SigningCertificateTemplate
 - IOCSPCAConfiguration.get_SigningCertificateTemplate
 - IOCSPCAConfiguration.put_SigningCertificateTemplate
 - IOCSPCAConfiguration.SigningCertificateTemplate
---

# IOCSPCAConfiguration::get_SigningCertificateTemplate


## -description

The <b>SigningCertificateTemplate</b> property gets or sets the template name for a signing certificate.

The <b>SigningCertificateTemplate</b> property contains a template name. This name is used in an Online Certificate Status Protocol (OCSP) signing-certificate renewal to specify the certificate version being requested.

This property supports enrollment or renewal of signing certificates that were signed by a replaced certificate key.

This property is read/write.

## -parameters

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-iocspcaconfiguration">IOCSPCAConfiguration</a>
