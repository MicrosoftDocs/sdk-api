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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOCSPCAConfiguration::get_KeySpec


## -description


The <b>KeySpec</b> property gets a value that indicates whether the key bound to the configuration is used for encryption or for signing content. The default implementations of <a href="https://msdn.microsoft.com/cf76e934-07a2-46de-b2cf-7f6d3e274d71">IOCSPAdmin</a> and <a href="https://msdn.microsoft.com/4e232c34-b5ab-4269-903b-189aac5a8ddc">IOCSPCAConfigurationCollection</a> methods set this value.

 Possible values are determined by the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) in use.

This property is read-only.


## -parameters


## -remarks



For the Microsoft Base Cryptographic Provider, the <b>KeySpec</b> property has the value <b>AT_KEYEXCHANGE</b> for <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">exchange keys</a> and the value <b>AT_SIGNATURE</b> for signature keys. The default value is <b>AT_SIGNATURE</b>.

For information about the other Microsoft CSPs, see 
<a href="https://msdn.microsoft.com/4e6eb2df-a917-4533-b9f1-8da39598d0b8">Cryptographic Service Providers</a> in the CryptoAPI 2.0 documentation.

For information about a non-Microsoft CSP, see the documentation provided with that CSP.




## -see-also




<a href="https://msdn.microsoft.com/57900e1e-9c51-4c1b-aa42-634b6c3a9999">IOCSPCAConfiguration</a>
 

 

