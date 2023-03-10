---
UID: NN:certadm.IOCSPCAConfigurationCollection
title: IOCSPCAConfigurationCollection (certadm.h)
description: Represents a set of certificates for which an Online Certificate Status Protocol (OCSP) service has been configured to provide certificate status responses.
helpviewer_keywords: ["IOCSPCAConfigurationCollection","IOCSPCAConfigurationCollection interface [Security]","IOCSPCAConfigurationCollection interface [Security]","described","certadm/IOCSPCAConfigurationCollection","security.iocspcaconfigurationcollection"]
old-location: security\iocspcaconfigurationcollection.htm
tech.root: security
ms.assetid: 4e232c34-b5ab-4269-903b-189aac5a8ddc
ms.date: 12/05/2018
ms.keywords: IOCSPCAConfigurationCollection, IOCSPCAConfigurationCollection interface [Security], IOCSPCAConfigurationCollection interface [Security],described, certadm/IOCSPCAConfigurationCollection, security.iocspcaconfigurationcollection
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
 - IOCSPCAConfigurationCollection
 - certadm/IOCSPCAConfigurationCollection
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
 - IOCSPCAConfigurationCollection
---

# IOCSPCAConfigurationCollection interface


## -description

The <b>IOCSPCAConfigurationCollection</b> interface represents a set of certificates for which an Online Certificate Status Protocol (OCSP) service has been configured to provide certificate status responses.

Microsoft provides a default implementation of this interface in the <b>OCSPCAConfigurationCollection</b> class. A <b>OCSPCAConfigurationCollection</b> object cannot be created externally.

The default implementation of <b>IOCSPAdmin</b> creates a <b>OCSPCAConfiguration</b> object and uses its properties.

## -inheritance

The <b>IOCSPCAConfigurationCollection</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IOCSPCAConfigurationCollection</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
