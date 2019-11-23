---
UID: NN:certadm.IOCSPProperty
title: IOCSPProperty (certadm.h)

description: Represents a name-value pair for OCSPServiceProperties or ProviderProperties.
old-location: security\iocspproperty.htm
tech.root: SecCrypto
ms.assetid: 854848f0-ea89-4c25-a8a5-40f1e4d229be

ms.date: 12/05/2018
ms.keywords: IOCSPProperty, IOCSPProperty interface [Security], IOCSPProperty interface [Security],described, certadm/IOCSPProperty, security.iocspproperty
ms.topic: interface
f1_keywords: 
 - "certadm/IOCSPProperty"
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
 - IOCSPProperty
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOCSPProperty interface


## -description


The <b>IOCSPProperty</b> interface represents a name-value pair for <a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-iocspadmin-get_ocspserviceproperties">OCSPServiceProperties</a> or <a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-iocspcaconfiguration-get_providerproperties">ProviderProperties</a>.

Microsoft provides a default implementation of this interface in the <b>OCSPProperty</b> class. An <b>OCSPProperty</b> object cannot be created externally.

The default implementation of <a href="https://docs.microsoft.com/windows/desktop/api/certadm/nn-certadm-iocsppropertycollection">IOCSPPropertyCollection</a> methods creates an <b>OCSPProperty</b> object and uses its properties.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

