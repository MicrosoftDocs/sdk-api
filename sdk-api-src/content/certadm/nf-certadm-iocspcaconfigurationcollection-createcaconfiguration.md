---
UID: NF:certadm.IOCSPCAConfigurationCollection.CreateCAConfiguration
title: IOCSPCAConfigurationCollection::CreateCAConfiguration (certadm.h)
description: Creates a new certification authority (CA) configuration and adds it to the configuration set.
helpviewer_keywords: ["CreateCAConfiguration","CreateCAConfiguration method [Security]","CreateCAConfiguration method [Security]","IOCSPCAConfigurationCollection interface","IOCSPCAConfigurationCollection interface [Security]","CreateCAConfiguration method","IOCSPCAConfigurationCollection.CreateCAConfiguration","IOCSPCAConfigurationCollection::CreateCAConfiguration","certadm/IOCSPCAConfigurationCollection::CreateCAConfiguration","security.iocspcaconfigurationcollection_createcaconfiguration_method"]
old-location: security\iocspcaconfigurationcollection_createcaconfiguration_method.htm
tech.root: security
ms.assetid: d1c47402-77b1-4c43-8d57-20b9dd2682f7
ms.date: 12/05/2018
ms.keywords: CreateCAConfiguration, CreateCAConfiguration method [Security], CreateCAConfiguration method [Security],IOCSPCAConfigurationCollection interface, IOCSPCAConfigurationCollection interface [Security],CreateCAConfiguration method, IOCSPCAConfigurationCollection.CreateCAConfiguration, IOCSPCAConfigurationCollection::CreateCAConfiguration, certadm/IOCSPCAConfigurationCollection::CreateCAConfiguration, security.iocspcaconfigurationcollection_createcaconfiguration_method
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
 - IOCSPCAConfigurationCollection::CreateCAConfiguration
 - certadm/IOCSPCAConfigurationCollection::CreateCAConfiguration
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
 - IOCSPCAConfigurationCollection.CreateCAConfiguration
---

# IOCSPCAConfigurationCollection::CreateCAConfiguration


## -description

The <b>CreateCAConfiguration</b> method creates a new <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) configuration and adds it to the configuration set.

## -parameters

### -param bstrIdentifier [in]

A string that contains a name for the new <a href="/windows/desktop/api/certadm/nn-certadm-iocspcaconfiguration">IOCSPCAConfiguration</a> object.

### -param varCACert [in]

An X.509 CA certificate.

### -param ppVal [out]

The address of a pointer to an <a href="/windows/desktop/api/certadm/nn-certadm-iocspcaconfiguration">IOCSPCAConfiguration</a> interface for the newly created object.

## -returns

<h3>C++</h3>
If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.



<h3>VB</h3>
An 
<a href="/windows/desktop/api/certadm/nn-certadm-iocspcaconfiguration">IOCSPCAConfiguration</a>
 interface for the newly created object.

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-iocspcaconfigurationcollection">IOCSPCAConfigurationCollection</a>