---
UID: NF:certadm.IOCSPCAConfiguration.get_CSPName
title: IOCSPCAConfiguration::get_CSPName
author: windows-sdk-content
description: Gets a cryptographic service provider (CSP) or key storage provider (KSP) name.
old-location: security\iocspcaconfiguration_cspname_method.htm
tech.root: seccrypto
ms.assetid: a35400a9-7eb7-4298-b023-efe2a087ba7d
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: CSPName property [Security], CSPName property [Security],IOCSPCAConfiguration interface, IOCSPCAConfiguration interface [Security],CSPName property, IOCSPCAConfiguration.CSPName, IOCSPCAConfiguration.get_CSPName, IOCSPCAConfiguration::CSPName, IOCSPCAConfiguration::get_CSPName, certadm/IOCSPCAConfiguration::CSPName, certadm/IOCSPCAConfiguration::get_CSPName, get_CSPName, security.iocspcaconfiguration_cspname_method
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
 - IOCSPCAConfiguration.CSPName
 - IOCSPCAConfiguration.get_CSPName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCSPCAConfiguration::get_CSPName


## -description


The <b>CSPName</b> property gets a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">cryptographic service provider</a> (CSP) or <a href="https://msdn.microsoft.com/en-us/library/ms721590(v=VS.85).aspx">key storage provider</a> (KSP) name. The default implementations of <a href="https://msdn.microsoft.com/en-us/library/Aa386313(v=VS.85).aspx">IOCSPAdmin</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa386330(v=VS.85).aspx">IOCSPCAConfigurationCollection</a> set this value.

This property is read-only.


## -parameters


## -remarks



The name returned in <i>pVal</i> corresponds to the CSP or KSP used for the <a href="https://msdn.microsoft.com/en-us/library/Aa386381(v=VS.85).aspx">SigningCertificate</a> property.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa386328(v=VS.85).aspx">IOCSPCAConfiguration</a>
 

 

