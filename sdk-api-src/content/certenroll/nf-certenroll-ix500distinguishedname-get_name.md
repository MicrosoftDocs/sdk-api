---
UID: NF:certenroll.IX500DistinguishedName.get_Name
title: IX500DistinguishedName::get_Name (certenroll.h)
description: Retrieves a distinguished name.
helpviewer_keywords: ["IX500DistinguishedName interface [Security]","Name property","IX500DistinguishedName.Name","IX500DistinguishedName.get_Name","IX500DistinguishedName::Name","IX500DistinguishedName::get_Name","Name property [Security]","Name property [Security]","IX500DistinguishedName interface","certenroll/IX500DistinguishedName::Name","certenroll/IX500DistinguishedName::get_Name","get_Name","security.ix500distinguishedname_name_property"]
old-location: security\ix500distinguishedname_name_property.htm
tech.root: security
ms.assetid: 1335c726-c16a-4a15-b231-8a3bd212f4ec
ms.date: 12/05/2018
ms.keywords: IX500DistinguishedName interface [Security],Name property, IX500DistinguishedName.Name, IX500DistinguishedName.get_Name, IX500DistinguishedName::Name, IX500DistinguishedName::get_Name, Name property [Security], Name property [Security],IX500DistinguishedName interface, certenroll/IX500DistinguishedName::Name, certenroll/IX500DistinguishedName::get_Name, get_Name, security.ix500distinguishedname_name_property
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
 - IX500DistinguishedName::get_Name
 - certenroll/IX500DistinguishedName::get_Name
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
 - IX500DistinguishedName.Name
 - IX500DistinguishedName.get_Name
---

# IX500DistinguishedName::get_Name


## -description

The <b>Name</b> property retrieves a distinguished name.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix500distinguishedname-encode">Encode</a> method to encode a distinguished name. Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix500distinguishedname-decode">Decode</a> method to decode a distinguished name. Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix500distinguishedname-get_encodedname">EncodedName</a> property to retrieve the name as an encoded string.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix500distinguishedname">IX500DistinguishedName</a>