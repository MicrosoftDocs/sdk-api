---
UID: NF:certadm.IOCSPCAConfiguration.get_CSPName
title: IOCSPCAConfiguration::get_CSPName
author: windows-sdk-content
description: Gets a cryptographic service provider (CSP) or key storage provider (KSP) name.
old-location: security\iocspcaconfiguration_cspname_method.htm
old-project: seccrypto
ms.assetid: a35400a9-7eb7-4298-b023-efe2a087ba7d
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: CSPName property [Security], CSPName property [Security],IOCSPCAConfiguration interface, IOCSPCAConfiguration interface [Security],CSPName property, IOCSPCAConfiguration.CSPName, IOCSPCAConfiguration.get_CSPName, IOCSPCAConfiguration::CSPName, IOCSPCAConfiguration::get_CSPName, certadm/IOCSPCAConfiguration::CSPName, certadm/IOCSPCAConfiguration::get_CSPName, get_CSPName, security.iocspcaconfiguration_cspname_method
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
 - IOCSPCAConfiguration.CSPName
 - IOCSPCAConfiguration.get_CSPName
product: Windows
targetos: Windows
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
---

# IOCSPCAConfiguration::get_CSPName


## -description


The <b>CSPName</b> property gets a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) or <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key storage provider</a> (KSP) name. The default implementations of <a href="https://msdn.microsoft.com/cf76e934-07a2-46de-b2cf-7f6d3e274d71">IOCSPAdmin</a> and <a href="https://msdn.microsoft.com/4e232c34-b5ab-4269-903b-189aac5a8ddc">IOCSPCAConfigurationCollection</a> set this value.

This property is read-only.


## -parameters


## -remarks



The name returned in <i>pVal</i> corresponds to the CSP or KSP used for the <a href="https://msdn.microsoft.com/8635c9f0-3c70-4037-8633-7a3440aff6c8">SigningCertificate</a> property.




## -see-also




<a href="https://msdn.microsoft.com/57900e1e-9c51-4c1b-aa42-634b6c3a9999">IOCSPCAConfiguration</a>
 

 

