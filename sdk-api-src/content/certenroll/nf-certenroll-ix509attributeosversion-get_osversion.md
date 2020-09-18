---
UID: NF:certenroll.IX509AttributeOSVersion.get_OSVersion
title: IX509AttributeOSVersion::get_OSVersion (certenroll.h)
description: Retrieves the client operating system version information.
helpviewer_keywords: ["IX509AttributeOSVersion interface [Security]","OSVersion property","IX509AttributeOSVersion.OSVersion","IX509AttributeOSVersion.get_OSVersion","IX509AttributeOSVersion::OSVersion","IX509AttributeOSVersion::get_OSVersion","OSVersion property [Security]","OSVersion property [Security]","IX509AttributeOSVersion interface","certenroll/IX509AttributeOSVersion::OSVersion","certenroll/IX509AttributeOSVersion::get_OSVersion","get_OSVersion","security.ix509attributeosversioner_osversion_property"]
old-location: security\ix509attributeosversioner_osversion_property.htm
tech.root: security
ms.assetid: 395ec2be-fe92-4bf1-bed3-db122e22f15e
ms.date: 12/05/2018
ms.keywords: IX509AttributeOSVersion interface [Security],OSVersion property, IX509AttributeOSVersion.OSVersion, IX509AttributeOSVersion.get_OSVersion, IX509AttributeOSVersion::OSVersion, IX509AttributeOSVersion::get_OSVersion, OSVersion property [Security], OSVersion property [Security],IX509AttributeOSVersion interface, certenroll/IX509AttributeOSVersion::OSVersion, certenroll/IX509AttributeOSVersion::get_OSVersion, get_OSVersion, security.ix509attributeosversioner_osversion_property
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509AttributeOSVersion::get_OSVersion
 - certenroll/IX509AttributeOSVersion::get_OSVersion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509AttributeOSVersion.OSVersion
 - IX509AttributeOSVersion.get_OSVersion
---

# IX509AttributeOSVersion::get_OSVersion


## -description

The <b>OSVersion</b> property retrieves the client operating system version information.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributeosversion-initializeencode">InitializeEncode</a> method or the  <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributeosversion-initializedecode">InitializeDecode</a> method to initialize the <b>OSVersion</b> property.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeosversion">IX509AttributeOSVersion</a>