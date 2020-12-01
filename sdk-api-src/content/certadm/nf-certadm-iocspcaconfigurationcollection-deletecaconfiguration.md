---
UID: NF:certadm.IOCSPCAConfigurationCollection.DeleteCAConfiguration
title: IOCSPCAConfigurationCollection::DeleteCAConfiguration (certadm.h)
description: Removes a named certification authority (CA) configuration from the configuration set.
helpviewer_keywords: ["DeleteCAConfiguration","DeleteCAConfiguration method [Security]","DeleteCAConfiguration method [Security]","IOCSPCAConfigurationCollection interface","IOCSPCAConfigurationCollection interface [Security]","DeleteCAConfiguration method","IOCSPCAConfigurationCollection.DeleteCAConfiguration","IOCSPCAConfigurationCollection::DeleteCAConfiguration","certadm/IOCSPCAConfigurationCollection::DeleteCAConfiguration","security.iocspcaconfigurationcollection_deletecaconfiguration_method"]
old-location: security\iocspcaconfigurationcollection_deletecaconfiguration_method.htm
tech.root: security
ms.assetid: 3733d98c-d262-4083-bac9-109720059f0b
ms.date: 12/05/2018
ms.keywords: DeleteCAConfiguration, DeleteCAConfiguration method [Security], DeleteCAConfiguration method [Security],IOCSPCAConfigurationCollection interface, IOCSPCAConfigurationCollection interface [Security],DeleteCAConfiguration method, IOCSPCAConfigurationCollection.DeleteCAConfiguration, IOCSPCAConfigurationCollection::DeleteCAConfiguration, certadm/IOCSPCAConfigurationCollection::DeleteCAConfiguration, security.iocspcaconfigurationcollection_deletecaconfiguration_method
req.header: certadm.h
req.include-header: Certsrv.h
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
 - IOCSPCAConfigurationCollection::DeleteCAConfiguration
 - certadm/IOCSPCAConfigurationCollection::DeleteCAConfiguration
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
 - IOCSPCAConfigurationCollection.DeleteCAConfiguration
---

# IOCSPCAConfigurationCollection::DeleteCAConfiguration


## -description

The <b>DeleteCAConfiguration</b> method removes a named <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) configuration from the configuration set.

## -parameters

### -param bstrIdentifier [in]

A string that contains the name for the <a href="/windows/desktop/api/certadm/nn-certadm-iocspcaconfiguration">IOCSPCAConfiguration</a> object.

## -remarks

The <i>bstrIdentifier</i> value must be one previously set by the <a href="/windows/desktop/api/certadm/nf-certadm-iocspcaconfigurationcollection-createcaconfiguration">CreateCAConfiguration</a> method.

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-iocspcaconfigurationcollection">IOCSPCAConfigurationCollection</a>