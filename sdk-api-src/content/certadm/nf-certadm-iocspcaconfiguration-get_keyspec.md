---
UID: NF:certadm.IOCSPCAConfiguration.get_KeySpec
title: IOCSPCAConfiguration::get_KeySpec (certadm.h)
author: windows-sdk-content
description: Gets a value that indicates whether the key bound to the configuration is used for encryption or for signing content.
old-location: security\iocspcaconfiguration_keyspec_method.htm
tech.root: SecCrypto
ms.assetid: 86f1e52f-bce2-497c-98e7-848ffc3243a0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOCSPCAConfiguration interface [Security],KeySpec property, IOCSPCAConfiguration.KeySpec, IOCSPCAConfiguration.get_KeySpec, IOCSPCAConfiguration::KeySpec, IOCSPCAConfiguration::get_KeySpec, KeySpec property [Security], KeySpec property [Security],IOCSPCAConfiguration interface, certadm/IOCSPCAConfiguration::KeySpec, certadm/IOCSPCAConfiguration::get_KeySpec, get_KeySpec, security.iocspcaconfiguration_keyspec_method
ms.topic: method
f1_keywords: 
 - "certadm/IOCSPCAConfiguration.KeySpec"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IOCSPCAConfiguration.KeySpec
 - IOCSPCAConfiguration.get_KeySpec
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOCSPCAConfiguration::get_KeySpec


## -description


The <b>KeySpec</b> property gets a value that indicates whether the key bound to the configuration is used for encryption or for signing content. The default implementations of <a href="https://docs.microsoft.com/windows/desktop/api/certadm/nn-certadm-iocspadmin">IOCSPAdmin</a> and <a href="https://docs.microsoft.com/windows/desktop/api/certadm/nn-certadm-iocspcaconfigurationcollection">IOCSPCAConfigurationCollection</a> methods set this value.

 Possible values are determined by the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) in use.

This property is read-only.


## -parameters


## -remarks



For the Microsoft Base Cryptographic Provider, the <b>KeySpec</b> property has the value <b>AT_KEYEXCHANGE</b> for <a href="https://docs.microsoft.com/windows/desktop/SecGloss/e-gly">exchange keys</a> and the value <b>AT_SIGNATURE</b> for signature keys. The default value is <b>AT_SIGNATURE</b>.

For information about the other Microsoft CSPs, see 
<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/cryptographic-service-providers">Cryptographic Service Providers</a> in the CryptoAPI 2.0 documentation.

For information about a non-Microsoft CSP, see the documentation provided with that CSP.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nn-certadm-iocspcaconfiguration">IOCSPCAConfiguration</a>
 

 

