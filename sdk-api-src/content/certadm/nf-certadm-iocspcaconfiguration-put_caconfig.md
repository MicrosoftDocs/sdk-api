---
UID: NF:certadm.IOCSPCAConfiguration.put_CAConfig
title: IOCSPCAConfiguration::put_CAConfig (certadm.h)
description: Gets or sets a certification authority (CA) name with which a signing certificate must be signed. (Put)
helpviewer_keywords: ["CAConfig property [Security]","CAConfig property [Security]","IOCSPCAConfiguration interface","IOCSPCAConfiguration interface [Security]","CAConfig property","IOCSPCAConfiguration.CAConfig","IOCSPCAConfiguration.put_CAConfig","IOCSPCAConfiguration::CAConfig","IOCSPCAConfiguration::get_CAConfig","IOCSPCAConfiguration::put_CAConfig","certadm/IOCSPCAConfiguration::CAConfig","certadm/IOCSPCAConfiguration::get_CAConfig","certadm/IOCSPCAConfiguration::put_CAConfig","put_CAConfig","security.iocspcaconfiguration_caconfig"]
old-location: security\iocspcaconfiguration_caconfig.htm
tech.root: security
ms.assetid: 642f8d0b-8dae-41a7-a87c-2b55d1034328
ms.date: 12/05/2018
ms.keywords: CAConfig property [Security], CAConfig property [Security],IOCSPCAConfiguration interface, IOCSPCAConfiguration interface [Security],CAConfig property, IOCSPCAConfiguration.CAConfig, IOCSPCAConfiguration.put_CAConfig, IOCSPCAConfiguration::CAConfig, IOCSPCAConfiguration::get_CAConfig, IOCSPCAConfiguration::put_CAConfig, certadm/IOCSPCAConfiguration::CAConfig, certadm/IOCSPCAConfiguration::get_CAConfig, certadm/IOCSPCAConfiguration::put_CAConfig, put_CAConfig, security.iocspcaconfiguration_caconfig
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
 - IOCSPCAConfiguration::put_CAConfig
 - certadm/IOCSPCAConfiguration::put_CAConfig
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
 - IOCSPCAConfiguration.CAConfig
 - IOCSPCAConfiguration.get_CAConfig
 - IOCSPCAConfiguration.put_CAConfig
---

# IOCSPCAConfiguration::put_CAConfig


## -description

The <b>CAConfig</b> property gets or sets a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) name with which a signing certificate must be signed.

The <b>CAConfig</b> property contains a CA name. This name lets an Online Certificate Status Protocol (OCSP) signing-certificate renewal request specify the issuing CA. The new signing certificate must be signed with this CA.

This property supports responses to status requests for a certificate that has been replaced but is still valid.

This property is read/write.

## -parameters

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-iocspcaconfiguration">IOCSPCAConfiguration</a>
