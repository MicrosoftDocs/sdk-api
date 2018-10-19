---
UID: NF:certadm.IOCSPCAConfiguration.get_CAConfig
title: IOCSPCAConfiguration::get_CAConfig
author: windows-sdk-content
description: Gets or sets a certification authority (CA) name with which a signing certificate must be signed.
old-location: security\iocspcaconfiguration_caconfig.htm
tech.root: seccrypto
ms.assetid: 642f8d0b-8dae-41a7-a87c-2b55d1034328
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: CAConfig property [Security], CAConfig property [Security],IOCSPCAConfiguration interface, IOCSPCAConfiguration interface [Security],CAConfig property, IOCSPCAConfiguration.CAConfig, IOCSPCAConfiguration.get_CAConfig, IOCSPCAConfiguration::CAConfig, IOCSPCAConfiguration::get_CAConfig, IOCSPCAConfiguration::put_CAConfig, certadm/IOCSPCAConfiguration::CAConfig, certadm/IOCSPCAConfiguration::get_CAConfig, certadm/IOCSPCAConfiguration::put_CAConfig, get_CAConfig, security.iocspcaconfiguration_caconfig
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
 - IOCSPCAConfiguration.CAConfig
 - IOCSPCAConfiguration.get_CAConfig
 - IOCSPCAConfiguration.put_CAConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCSPCAConfiguration::get_CAConfig


## -description


The <b>CAConfig</b> property gets or sets a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) name with which a signing certificate must be signed.

The <b>CAConfig</b> property contains a CA name. This name lets an Online Certificate Status Protocol (OCSP) signing-certificate renewal request specify the issuing CA. The new signing certificate must be signed with this CA.

This property supports responses to status requests for a certificate that has been replaced but is still valid.

This property is read/write.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/57900e1e-9c51-4c1b-aa42-634b6c3a9999">IOCSPCAConfiguration</a>
 

 

