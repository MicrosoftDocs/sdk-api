---
UID: NF:certadm.IOCSPCAConfiguration.get_CACertificate
title: IOCSPCAConfiguration::get_CACertificate
author: windows-sdk-content
description: Gets an X.509 certificate that has been encoded by using Distinguished Encoding Rules (DER) and that is for a certification authority (CA).
old-location: security\iocspcaconfiguration_cacertificate_method.htm
tech.root: SecCrypto
ms.assetid: 73fd56d2-a0d4-4bf8-b818-aadf8cbac9c4
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CACertificate property [Security], CACertificate property [Security],IOCSPCAConfiguration interface, IOCSPCAConfiguration interface [Security],CACertificate property, IOCSPCAConfiguration.CACertificate, IOCSPCAConfiguration.get_CACertificate, IOCSPCAConfiguration::CACertificate, IOCSPCAConfiguration::get_CACertificate, certadm/IOCSPCAConfiguration::CACertificate, certadm/IOCSPCAConfiguration::get_CACertificate, get_CACertificate, security.iocspcaconfiguration_cacertificate_method
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
 - IOCSPCAConfiguration.CACertificate
 - IOCSPCAConfiguration.get_CACertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCSPCAConfiguration::get_CACertificate


## -description


The <b>CACertificate</b> property gets an X.509 certificate that has been encoded by using <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) and that is for a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> (CA). The default implementations of <a href="https://msdn.microsoft.com/en-us/library/Aa386313(v=VS.85).aspx">IOCSPAdmin</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa386330(v=VS.85).aspx">IOCSPCAConfigurationCollection</a> methods set this value.

This property is read-only.


## -parameters


## -remarks



The <i>pVal</i> certificate corresponds to the certificate used in the <i>varCACert</i> parameter of the <a href="https://msdn.microsoft.com/en-us/library/Aa386335(v=VS.85).aspx">CreateCAConfiguration</a> method to create the configuration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa386313(v=VS.85).aspx">IOCSPCAConfiguration</a>
 

 

