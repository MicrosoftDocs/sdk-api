---
UID: NF:xenroll.IEnroll4.addBlobPropertyToCertificateWStr
title: IEnroll4::addBlobPropertyToCertificateWStr (xenroll.h)
description: The IEnroll4::addBlobPropertyToCertificateWStr method adds a BLOB property to a certificate.
helpviewer_keywords: ["IEnroll4 interface [Security]","addBlobPropertyToCertificateWStr method","IEnroll4.addBlobPropertyToCertificateWStr","IEnroll4::addBlobPropertyToCertificateWStr","addBlobPropertyToCertificateWStr","addBlobPropertyToCertificateWStr method [Security]","addBlobPropertyToCertificateWStr method [Security]","IEnroll4 interface","security.ienroll4_addblobpropertytocertificatewstr","xenroll/IEnroll4::addBlobPropertyToCertificateWStr"]
old-location: security\ienroll4_addblobpropertytocertificatewstr.htm
tech.root: security
ms.assetid: 954c1b2f-08ea-471c-902f-1aa5523d58b3
ms.date: 12/05/2018
ms.keywords: IEnroll4 interface [Security],addBlobPropertyToCertificateWStr method, IEnroll4.addBlobPropertyToCertificateWStr, IEnroll4::addBlobPropertyToCertificateWStr, addBlobPropertyToCertificateWStr, addBlobPropertyToCertificateWStr method [Security], addBlobPropertyToCertificateWStr method [Security],IEnroll4 interface, security.ienroll4_addblobpropertytocertificatewstr, xenroll/IEnroll4::addBlobPropertyToCertificateWStr
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
 - IEnroll4::addBlobPropertyToCertificateWStr
 - xenroll/IEnroll4::addBlobPropertyToCertificateWStr
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
 - IEnroll4.addBlobPropertyToCertificateWStr
---

# IEnroll4::addBlobPropertyToCertificateWStr


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>addBlobPropertyToCertificateWStr</b> method adds a <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> property to a certificate. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a> interface.

## -parameters

### -param lPropertyId [in]

The identifier of the BLOB property to add to the certificate.

### -param lReserved [in]

This parameter is reserved. Must be zero.

### -param pBlobProperty [in]

A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that represents the data for  the BLOB property.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a>