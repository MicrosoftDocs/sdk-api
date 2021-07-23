---
UID: NN:certadm.IOCSPPropertyCollection
title: IOCSPPropertyCollection (certadm.h)
description: Represents a set of configurable attribute properties (name-value pairs) for an Online Certificate Status Protocol (OCSP) service.
helpviewer_keywords: ["IOCSPPropertyCollection","IOCSPPropertyCollection interface [Security]","IOCSPPropertyCollection interface [Security]","described","certadm/IOCSPPropertyCollection","security.iocsppropertycollection"]
old-location: security\iocsppropertycollection.htm
tech.root: security
ms.assetid: 8c700357-0cb4-4780-9ff1-ac57c46f9183
ms.date: 12/05/2018
ms.keywords: IOCSPPropertyCollection, IOCSPPropertyCollection interface [Security], IOCSPPropertyCollection interface [Security],described, certadm/IOCSPPropertyCollection, security.iocsppropertycollection
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
 - IOCSPPropertyCollection
 - certadm/IOCSPPropertyCollection
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
 - IOCSPPropertyCollection
---

# IOCSPPropertyCollection interface


## -description

The <b>IOCSPPropertyCollection</b> interface represents a set of configurable attribute properties (name-value pairs) for an Online Certificate Status Protocol (OCSP) service. Microsoft provides a default implementation of this interface in the <b>OCSPPropertyCollection</b> class.

In C++, you create an instance of this interface by calling the <b>CoCreateInstance</b> function with the <b>CLSID_OCSPPropertyCollection</b> class identifier.

In Visual Basic Scripting Edition, you create an instance of the <b>OCSPPropertyCollection</b> object.

## -inheritance

The <b>IOCSPPropertyCollection</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IOCSPPropertyCollection</b> also has these types of members:

## -remarks

The <b>IOCSPPropertyCollection</b> contains attributes for the following:

<ul>
<li>Web proxy settings that include the  number of threads and number of cache entries</li>
<li>Audit settings that include start/stop, configuration change, security change, and request events</li>
<li>Security settings that include ACEs for <a href="/windows/desktop/api/certadm/nn-certadm-iocspadmin">IOCSPAdmin</a> interfaces</li>
</ul>
All OCSP attribute information is stored in the following registry key:


<b>HKEY_LOCAL_MACHINE</b>&#92;<b>SYSTEM</b>&#92;<b>CurrentControlSet</b>&#92;<b>Services</b>&#92;<b>OCSPSvc</b>&#92;<b>Responder</b>



OCSP attributes govern OCSP responder service behavior for all CA configurations. For more information on CA configurations, see the <a href="/windows/desktop/api/certadm/nn-certadm-iocspcaconfiguration">IOCSPCAConfiguration</a> interface topic.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
