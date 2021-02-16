---
UID: NF:certadm.IOCSPProperty.get_Name
title: IOCSPProperty::get_Name (certadm.h)
description: Gets the identifier part of the name-value pair represented by an OCSPProperty object.
helpviewer_keywords: ["IOCSPProperty interface [Security]","Name property","IOCSPProperty.Name","IOCSPProperty.get_Name","IOCSPProperty::Name","IOCSPProperty::get_Name","Name property [Security]","Name property [Security]","IOCSPProperty interface","certadm/IOCSPProperty::Name","certadm/IOCSPProperty::get_Name","get_Name","security.iocspproperty_name_method"]
old-location: security\iocspproperty_name_method.htm
tech.root: security
ms.assetid: 33980a7c-0ae5-470b-a55a-f3e19c8846a6
ms.date: 12/05/2018
ms.keywords: IOCSPProperty interface [Security],Name property, IOCSPProperty.Name, IOCSPProperty.get_Name, IOCSPProperty::Name, IOCSPProperty::get_Name, Name property [Security], Name property [Security],IOCSPProperty interface, certadm/IOCSPProperty::Name, certadm/IOCSPProperty::get_Name, get_Name, security.iocspproperty_name_method
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
 - IOCSPProperty::get_Name
 - certadm/IOCSPProperty::get_Name
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
 - IOCSPProperty.Name
 - IOCSPProperty.get_Name
---

# IOCSPProperty::get_Name


## -description

The <b>Name</b> property gets the identifier part of the name-value pair represented by an <b>OCSPProperty</b> object.

This property is read-only.

## -parameters

## -remarks

For possible values of <i>pVal</i>, see <a href="/windows/desktop/api/certadm/nf-certadm-iocspadmin-get_ocspserviceproperties">OCSPServiceProperties</a> or <a href="/windows/desktop/api/certadm/nf-certadm-iocspcaconfiguration-get_providerproperties">ProviderProperties</a>.

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-iocspproperty">IOCSPProperty</a>