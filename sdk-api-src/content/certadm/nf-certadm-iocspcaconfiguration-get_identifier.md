---
UID: NF:certadm.IOCSPCAConfiguration.get_Identifier
title: IOCSPCAConfiguration::get_Identifier
author: windows-sdk-content
description: Gets a name for the certification authority (CA) configuration.
old-location: security\iocspcaconfiguration_identifier_method.htm
tech.root: seccrypto
ms.assetid: a35aaaf1-8bad-4de1-a2e8-2e4947c30d72
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: IOCSPCAConfiguration interface [Security],Identifier property, IOCSPCAConfiguration.Identifier, IOCSPCAConfiguration.get_Identifier, IOCSPCAConfiguration::Identifier, IOCSPCAConfiguration::get_Identifier, Identifier property [Security], Identifier property [Security],IOCSPCAConfiguration interface, certadm/IOCSPCAConfiguration::Identifier, certadm/IOCSPCAConfiguration::get_Identifier, get_Identifier, security.iocspcaconfiguration_identifier_method
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
 - IOCSPCAConfiguration.Identifier
 - IOCSPCAConfiguration.get_Identifier
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCSPCAConfiguration::get_Identifier


## -description


The <b>Identifier</b> property gets a name for the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> (CA) configuration. The default implementations of <a href="https://msdn.microsoft.com/en-us/library/Aa386313(v=VS.85).aspx">IOCSPAdmin</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa386330(v=VS.85).aspx">IOCSPCAConfigurationCollection</a> set this value.

This property is read-only.


## -parameters


## -remarks



The name returned in <i>pVal</i> corresponds to the name used in the <i>bstrIdentifier</i> parameter of the <a href="https://msdn.microsoft.com/en-us/library/Aa386335(v=VS.85).aspx">CreateCAConfiguration</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa386328(v=VS.85).aspx">IOCSPCAConfiguration</a>
 

 

