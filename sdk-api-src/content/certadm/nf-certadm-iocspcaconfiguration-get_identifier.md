---
UID: NF:certadm.IOCSPCAConfiguration.get_Identifier
title: IOCSPCAConfiguration::get_Identifier (certadm.h)
description: Gets a name for the certification authority (CA) configuration.
helpviewer_keywords: ["IOCSPCAConfiguration interface [Security]","Identifier property","IOCSPCAConfiguration.Identifier","IOCSPCAConfiguration.get_Identifier","IOCSPCAConfiguration::Identifier","IOCSPCAConfiguration::get_Identifier","Identifier property [Security]","Identifier property [Security]","IOCSPCAConfiguration interface","certadm/IOCSPCAConfiguration::Identifier","certadm/IOCSPCAConfiguration::get_Identifier","get_Identifier","security.iocspcaconfiguration_identifier_method"]
old-location: security\iocspcaconfiguration_identifier_method.htm
tech.root: security
ms.assetid: a35aaaf1-8bad-4de1-a2e8-2e4947c30d72
ms.date: 12/05/2018
ms.keywords: IOCSPCAConfiguration interface [Security],Identifier property, IOCSPCAConfiguration.Identifier, IOCSPCAConfiguration.get_Identifier, IOCSPCAConfiguration::Identifier, IOCSPCAConfiguration::get_Identifier, Identifier property [Security], Identifier property [Security],IOCSPCAConfiguration interface, certadm/IOCSPCAConfiguration::Identifier, certadm/IOCSPCAConfiguration::get_Identifier, get_Identifier, security.iocspcaconfiguration_identifier_method
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
 - IOCSPCAConfiguration::get_Identifier
 - certadm/IOCSPCAConfiguration::get_Identifier
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
 - IOCSPCAConfiguration.Identifier
 - IOCSPCAConfiguration.get_Identifier
---

# IOCSPCAConfiguration::get_Identifier


## -description

The <b>Identifier</b> property gets a name for the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) configuration. The default implementations of <a href="/windows/desktop/api/certadm/nn-certadm-iocspadmin">IOCSPAdmin</a> and <a href="/windows/desktop/api/certadm/nn-certadm-iocspcaconfigurationcollection">IOCSPCAConfigurationCollection</a> set this value.

This property is read-only.

## -parameters

## -remarks

The name returned in <i>pVal</i> corresponds to the name used in the <i>bstrIdentifier</i> parameter of the <a href="/windows/desktop/api/certadm/nf-certadm-iocspcaconfigurationcollection-createcaconfiguration">CreateCAConfiguration</a> method.

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-iocspcaconfiguration">IOCSPCAConfiguration</a>