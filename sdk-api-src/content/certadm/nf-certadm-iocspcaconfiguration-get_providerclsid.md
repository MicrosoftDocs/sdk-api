---
UID: NF:certadm.IOCSPCAConfiguration.get_ProviderCLSID
title: IOCSPCAConfiguration::get_ProviderCLSID
author: windows-driver-content
description: Gets or sets the CLSID of the revocation information provider used by the CA configuration.
old-location: security\iocspcaconfiguration_providerclsid_method.htm
old-project: SecCrypto
ms.assetid: 4ea109a9-00ed-46b5-a58c-7dc5bc936102
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IOCSPCAConfiguration interface [Security],ProviderCLSID property, IOCSPCAConfiguration.ProviderCLSID, IOCSPCAConfiguration.get_ProviderCLSID, IOCSPCAConfiguration::ProviderCLSID, IOCSPCAConfiguration::get_ProviderCLSID, IOCSPCAConfiguration::put_ProviderCLSID, ProviderCLSID property [Security], ProviderCLSID property [Security],IOCSPCAConfiguration interface, certadm/IOCSPCAConfiguration::ProviderCLSID, certadm/IOCSPCAConfiguration::get_ProviderCLSID, certadm/IOCSPCAConfiguration::put_ProviderCLSID, get_ProviderCLSID, security.iocspcaconfiguration_providerclsid_method
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Certadm.dll
api_name:
-	IOCSPCAConfiguration.ProviderCLSID
-	IOCSPCAConfiguration.get_ProviderCLSID
-	IOCSPCAConfiguration.put_ProviderCLSID
product: Windows
targetos: Windows
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
---

# IOCSPCAConfiguration::get_ProviderCLSID


## -description


The <b>ProviderCLSID</b> property gets or sets the CLSID of the  revocation information provider used by the CA configuration. A provider implements <b>IOCSPRevInfoProvider</b> interface and processes certificate status requests for a responder service.

This property is read/write.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/57900e1e-9c51-4c1b-aa42-634b6c3a9999">IOCSPCAConfiguration</a>
 

 

