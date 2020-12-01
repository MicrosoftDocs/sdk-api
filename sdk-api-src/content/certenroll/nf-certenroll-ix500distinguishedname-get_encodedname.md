---
UID: NF:certenroll.IX500DistinguishedName.get_EncodedName
title: IX500DistinguishedName::get_EncodedName (certenroll.h)
description: Retrieves a Unicode-encoded distinguished name.
helpviewer_keywords: ["EncodedName property [Security]","EncodedName property [Security]","IX500DistinguishedName interface","IX500DistinguishedName interface [Security]","EncodedName property","IX500DistinguishedName.EncodedName","IX500DistinguishedName.get_EncodedName","IX500DistinguishedName::EncodedName","IX500DistinguishedName::get_EncodedName","certenroll/IX500DistinguishedName::EncodedName","certenroll/IX500DistinguishedName::get_EncodedName","get_EncodedName","security.ix500distinguishedname_encodedname_property"]
old-location: security\ix500distinguishedname_encodedname_property.htm
tech.root: security
ms.assetid: c3b2966c-5149-462d-908b-f6eca6a0409d
ms.date: 12/05/2018
ms.keywords: EncodedName property [Security], EncodedName property [Security],IX500DistinguishedName interface, IX500DistinguishedName interface [Security],EncodedName property, IX500DistinguishedName.EncodedName, IX500DistinguishedName.get_EncodedName, IX500DistinguishedName::EncodedName, IX500DistinguishedName::get_EncodedName, certenroll/IX500DistinguishedName::EncodedName, certenroll/IX500DistinguishedName::get_EncodedName, get_EncodedName, security.ix500distinguishedname_encodedname_property
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
 - IX500DistinguishedName::get_EncodedName
 - certenroll/IX500DistinguishedName::get_EncodedName
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
 - IX500DistinguishedName.EncodedName
 - IX500DistinguishedName.get_EncodedName
---

# IX500DistinguishedName::get_EncodedName


## -description

The <b>EncodedName</b> property retrieves a Unicode-encoded distinguished name.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix500distinguishedname-encode">Encode</a> method to encode a distinguished name. Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix500distinguishedname-decode">Decode</a> method to decode a distinguished name.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix500distinguishedname">IX500DistinguishedName</a>