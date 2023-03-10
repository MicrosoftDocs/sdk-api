---
UID: NF:xenroll.IEnroll4.addAttributeToRequestWStr
title: IEnroll4::addAttributeToRequestWStr (xenroll.h)
description: Adds an attribute to the certificate request.
helpviewer_keywords: ["IEnroll4 interface [Security]","addAttributeToRequestWStr method","IEnroll4.addAttributeToRequestWStr","IEnroll4::addAttributeToRequestWStr","addAttributeToRequestWStr","addAttributeToRequestWStr method [Security]","addAttributeToRequestWStr method [Security]","IEnroll4 interface","security.ienroll4_addattributetorequestwstr","xenroll/IEnroll4::addAttributeToRequestWStr"]
old-location: security\ienroll4_addattributetorequestwstr.htm
tech.root: security
ms.assetid: 71421bca-ef72-47d3-8f4a-95cb9768644f
ms.date: 12/05/2018
ms.keywords: IEnroll4 interface [Security],addAttributeToRequestWStr method, IEnroll4.addAttributeToRequestWStr, IEnroll4::addAttributeToRequestWStr, addAttributeToRequestWStr, addAttributeToRequestWStr method [Security], addAttributeToRequestWStr method [Security],IEnroll4 interface, security.ienroll4_addattributetorequestwstr, xenroll/IEnroll4::addAttributeToRequestWStr
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnroll4::addAttributeToRequestWStr
 - xenroll/IEnroll4::addAttributeToRequestWStr
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll4.addAttributeToRequestWStr
---

# IEnroll4::addAttributeToRequestWStr


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>addAttributeToRequestWStr</b> method adds an <a href="/windows/desktop/SecGloss/a-gly">attribute</a> to the <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a> interface.

## -parameters

### -param Flags [in]

This parameter is reserved for future use and must be set to zero.

### -param pwszName [in]

A pointer to a null-terminated wide character string that represents the object identifier (OID) for the attribute name.

### -param pblobValue [in]

A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that represents the attribute value.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a>