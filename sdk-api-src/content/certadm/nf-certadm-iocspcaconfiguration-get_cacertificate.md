---
UID: NF:certadm.IOCSPCAConfiguration.get_CACertificate
title: IOCSPCAConfiguration::get_CACertificate method
author: windows-driver-content
description: Gets an X.509 certificate that has been encoded by using Distinguished Encoding Rules (DER) and that is for a certification authority (CA).
old-location: security\iocspcaconfiguration_cacertificate_method.htm
old-project: SecCrypto
ms.assetid: 73fd56d2-a0d4-4bf8-b818-aadf8cbac9c4
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: CACertificate property [Security], CACertificate property [Security], IOCSPCAConfiguration interface, IOCSPCAConfiguration, IOCSPCAConfiguration interface [Security], CACertificate property, IOCSPCAConfiguration.CACertificate, IOCSPCAConfiguration::get_CACertificate, certadm/IOCSPCAConfiguration::CACertificate, certadm/IOCSPCAConfiguration::get_CACertificate, get_CACertificate,IOCSPCAConfiguration.get_CACertificate, security.iocspcaconfiguration_cacertificate_method
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
req.typenames: CHANNEL_ENTRY_POINTS, *PCHANNEL_ENTRY_POINTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Certadm.dll
api_name:
-	IOCSPCAConfiguration.CACertificate
-	IOCSPCAConfiguration.get_CACertificate
product: Windows
targetos: Windows
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
---

# IOCSPCAConfiguration::get_CACertificate method


## -description


The <b>CACertificate</b> property gets an X.509 certificate that has been encoded by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) and that is for a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA). The default implementations of <a href="https://msdn.microsoft.com/cf76e934-07a2-46de-b2cf-7f6d3e274d71">IOCSPAdmin</a> and <a href="https://msdn.microsoft.com/4e232c34-b5ab-4269-903b-189aac5a8ddc">IOCSPCAConfigurationCollection</a> methods set this value.

This property is read-only.


## -parameters


## -remarks



The <i>pVal</i> certificate corresponds to the certificate used in the <i>varCACert</i> parameter of the <a href="https://msdn.microsoft.com/d1c47402-77b1-4c43-8d57-20b9dd2682f7">CreateCAConfiguration</a> method to create the configuration.




## -see-also




<a href="https://msdn.microsoft.com/cf76e934-07a2-46de-b2cf-7f6d3e274d71">IOCSPCAConfiguration</a>
 

 

