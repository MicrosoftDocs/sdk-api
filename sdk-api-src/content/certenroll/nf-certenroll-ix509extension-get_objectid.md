---
UID: NF:certenroll.IX509Extension.get_ObjectId
title: IX509Extension::get_ObjectId (certenroll.h)
description: Retrieves the object identifier (OID) for the extension.
helpviewer_keywords: ["IX509Extension interface [Security]","ObjectId property","IX509Extension.ObjectId","IX509Extension.get_ObjectId","IX509Extension::ObjectId","IX509Extension::get_ObjectId","ObjectId property [Security]","ObjectId property [Security]","IX509Extension interface","certenroll/IX509Extension::ObjectId","certenroll/IX509Extension::get_ObjectId","get_ObjectId","security.ix509extension_objectid_property"]
old-location: security\ix509extension_objectid_property.htm
tech.root: security
ms.assetid: d3508bfe-e323-4075-9c82-d9b53b8f54aa
ms.date: 12/05/2018
ms.keywords: IX509Extension interface [Security],ObjectId property, IX509Extension.ObjectId, IX509Extension.get_ObjectId, IX509Extension::ObjectId, IX509Extension::get_ObjectId, ObjectId property [Security], ObjectId property [Security],IX509Extension interface, certenroll/IX509Extension::ObjectId, certenroll/IX509Extension::get_ObjectId, get_ObjectId, security.ix509extension_objectid_property
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
 - IX509Extension::get_ObjectId
 - certenroll/IX509Extension::get_ObjectId
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
 - IX509Extension.ObjectId
 - IX509Extension.get_ObjectId
---

# IX509Extension::get_ObjectId


## -description

The <b>ObjectId</b> property retrieves the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID)  for the extension.

This property is read-only.

## -parameters

## -remarks

You can specify the OID when you call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-initialize">Initialize</a> method to create an extension value.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>