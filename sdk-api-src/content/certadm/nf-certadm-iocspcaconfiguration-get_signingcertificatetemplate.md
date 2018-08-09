---
UID: NF:certadm.IOCSPCAConfiguration.get_SigningCertificateTemplate
title: IOCSPCAConfiguration::get_SigningCertificateTemplate
author: windows-sdk-content
description: Gets or sets the template name for a signing certificate.
old-location: security\iocspcaconfiguration_signingcertificatetemplate.htm
old-project: seccrypto
ms.assetid: 38e75d8f-1e6a-4214-8142-85f7e9c41ce2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IOCSPCAConfiguration interface [Security],SigningCertificateTemplate property, IOCSPCAConfiguration.SigningCertificateTemplate, IOCSPCAConfiguration.get_SigningCertificateTemplate, IOCSPCAConfiguration::SigningCertificateTemplate, IOCSPCAConfiguration::get_SigningCertificateTemplate, IOCSPCAConfiguration::put_SigningCertificateTemplate, SigningCertificateTemplate property [Security], SigningCertificateTemplate property [Security],IOCSPCAConfiguration interface, certadm/IOCSPCAConfiguration::SigningCertificateTemplate, certadm/IOCSPCAConfiguration::get_SigningCertificateTemplate, certadm/IOCSPCAConfiguration::put_SigningCertificateTemplate, get_SigningCertificateTemplate, security.iocspcaconfiguration_signingcertificatetemplate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
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
product: Windows
targetos: Windows
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
---

# IOCSPCAConfiguration::get_SigningCertificateTemplate


## -description


The <b>SigningCertificateTemplate</b> property gets or sets the template name for a signing certificate.

The <b>SigningCertificateTemplate</b> property contains a template name. This name is used in an Online Certificate Status Protocol (OCSP) signing-certificate renewal to specify the certificate version being requested.

This property supports enrollment or renewal of signing certificates that were signed by a replaced certificate key.

This property is read/write.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/57900e1e-9c51-4c1b-aa42-634b6c3a9999">IOCSPCAConfiguration</a>
 

 

