---
UID: NF:certadm.IOCSPCAConfiguration.get_ProviderCLSID
title: IOCSPCAConfiguration::get_ProviderCLSID (certadm.h)
description: Gets or sets the CLSID of the revocation information provider used by the CA configuration.helpviewer_keywords: ["IOCSPCAConfiguration interface [Security]","ProviderCLSID property","IOCSPCAConfiguration.ProviderCLSID","IOCSPCAConfiguration.get_ProviderCLSID","IOCSPCAConfiguration::ProviderCLSID","IOCSPCAConfiguration::get_ProviderCLSID","IOCSPCAConfiguration::put_ProviderCLSID","ProviderCLSID property [Security]","ProviderCLSID property [Security]","IOCSPCAConfiguration interface","certadm/IOCSPCAConfiguration::ProviderCLSID","certadm/IOCSPCAConfiguration::get_ProviderCLSID","certadm/IOCSPCAConfiguration::put_ProviderCLSID","get_ProviderCLSID","security.iocspcaconfiguration_providerclsid_method"]
old-location: security\iocspcaconfiguration_providerclsid_method.htm
tech.root: SecCrypto
ms.assetid: 4ea109a9-00ed-46b5-a58c-7dc5bc936102
ms.date: 12/05/2018
ms.keywords: IOCSPCAConfiguration interface [Security],ProviderCLSID property, IOCSPCAConfiguration.ProviderCLSID, IOCSPCAConfiguration.get_ProviderCLSID, IOCSPCAConfiguration::ProviderCLSID, IOCSPCAConfiguration::get_ProviderCLSID, IOCSPCAConfiguration::put_ProviderCLSID, ProviderCLSID property [Security], ProviderCLSID property [Security],IOCSPCAConfiguration interface, certadm/IOCSPCAConfiguration::ProviderCLSID, certadm/IOCSPCAConfiguration::get_ProviderCLSID, certadm/IOCSPCAConfiguration::put_ProviderCLSID, get_ProviderCLSID, security.iocspcaconfiguration_providerclsid_method
f1_keywords:
- certadm/IOCSPCAConfiguration.ProviderCLSID
dev_langs:
- c++
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
- IOCSPCAConfiguration.ProviderCLSID
- IOCSPCAConfiguration.get_ProviderCLSID
- IOCSPCAConfiguration.put_ProviderCLSID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOCSPCAConfiguration::get_ProviderCLSID


## -description


The <b>ProviderCLSID</b> property gets or sets the CLSID of the  revocation information provider used by the CA configuration. A provider implements <b>IOCSPRevInfoProvider</b> interface and processes certificate status requests for a responder service.

This property is read/write.


## -parameters


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nn-certadm-iocspcaconfiguration">IOCSPCAConfiguration</a>
 

 

