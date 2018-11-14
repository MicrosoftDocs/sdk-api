---
UID: NF:certadm.IOCSPCAConfiguration.get_KeySpec
title: IOCSPCAConfiguration::get_KeySpec
author: windows-sdk-content
description: Gets a value that indicates whether the key bound to the configuration is used for encryption or for signing content.
old-location: security\iocspcaconfiguration_keyspec_method.htm
tech.root: seccrypto
ms.assetid: 86f1e52f-bce2-497c-98e7-848ffc3243a0
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IOCSPCAConfiguration interface [Security],KeySpec property, IOCSPCAConfiguration.KeySpec, IOCSPCAConfiguration.get_KeySpec, IOCSPCAConfiguration::KeySpec, IOCSPCAConfiguration::get_KeySpec, KeySpec property [Security], KeySpec property [Security],IOCSPCAConfiguration interface, certadm/IOCSPCAConfiguration::KeySpec, certadm/IOCSPCAConfiguration::get_KeySpec, get_KeySpec, security.iocspcaconfiguration_keyspec_method
ms.prod: windows-hardware
ms.technology: windows-devices
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
- apiref
: 
- COM
: 
- certadm.h
: 
- IOCSPCAConfiguration.get_KeySpec
: 
---

# IOCSPCAConfiguration::get_KeySpec


## -description


The <b>KeySpec</b> property gets a value that indicates whether the key bound to the configuration is used for encryption or for signing content. The default implementations of <a href="https://msdn.microsoft.com/en-us/library/Aa386313(v=VS.85).aspx">IOCSPAdmin</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa386330(v=VS.85).aspx">IOCSPCAConfigurationCollection</a> methods set this value.

 Possible values are determined by the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">cryptographic service provider</a> (CSP) in use.

This property is read-only.


## -parameters


## -remarks



For the Microsoft Base Cryptographic Provider, the <b>KeySpec</b> property has the value <b>AT_KEYEXCHANGE</b> for <a href="https://msdn.microsoft.com/en-us/library/ms721575(v=VS.85).aspx">exchange keys</a> and the value <b>AT_SIGNATURE</b> for signature keys. The default value is <b>AT_SIGNATURE</b>.

For information about the other Microsoft CSPs, see 
<a href="https://msdn.microsoft.com/en-us/library/Aa380245(v=VS.85).aspx">Cryptographic Service Providers</a> in the CryptoAPI 2.0 documentation.

For information about a non-Microsoft CSP, see the documentation provided with that CSP.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa386328(v=VS.85).aspx">IOCSPCAConfiguration</a>
 

 

