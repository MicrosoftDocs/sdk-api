---
UID: NN:certadm.IOCSPCAConfiguration
title: IOCSPCAConfiguration (certadm.h)
description: Represents a set of definitions that enable an Online Certificate Status Protocol (OCSP) service to respond to a certificate status request for a specific certification authority (CA).
helpviewer_keywords: ["IOCSPCAConfiguration","IOCSPCAConfiguration interface [Security]","IOCSPCAConfiguration interface [Security]","described","certadm/IOCSPCAConfiguration","security.iocspcaconfiguration"]
old-location: security\iocspcaconfiguration.htm
tech.root: security
ms.assetid: 57900e1e-9c51-4c1b-aa42-634b6c3a9999
ms.date: 12/05/2018
ms.keywords: IOCSPCAConfiguration, IOCSPCAConfiguration interface [Security], IOCSPCAConfiguration interface [Security],described, certadm/IOCSPCAConfiguration, security.iocspcaconfiguration
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
 - IOCSPCAConfiguration
 - certadm/IOCSPCAConfiguration
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
 - IOCSPCAConfiguration
---

# IOCSPCAConfiguration interface


## -description

The <b>IOCSPCAConfiguration</b> interface represents a set of definitions that enable an Online Certificate Status Protocol (OCSP) service to respond to a certificate status request for a specific <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA).

Microsoft provides a default implementation of this interface in the <b>OCSPCAConfiguration</b> class. An <b>OCSPCAConfiguration</b> object cannot be created externally. An <b>OCSPCAConfiguration</b> object can only be created by using the <a href="/windows/desktop/api/certadm/nf-certadm-iocspcaconfigurationcollection-createcaconfiguration">CreateCAConfiguration</a> method.

 The default implementations of <a href="/windows/desktop/api/certadm/nn-certadm-iocspadmin">IOCSPAdmin</a> and <a href="/windows/desktop/api/certadm/nn-certadm-iocspcaconfigurationcollection">IOCSPCAConfigurationCollection</a> methods create a <b>OCSPCAConfiguration</b> object and use its properties.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>