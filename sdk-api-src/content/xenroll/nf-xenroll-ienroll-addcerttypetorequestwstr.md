---
UID: NF:xenroll.IEnroll.AddCertTypeToRequestWStr
title: IEnroll::AddCertTypeToRequestWStr (xenroll.h)
description: Adds a certificate template to a request (used to support the enterprise certification authority (CA)).
helpviewer_keywords: ["AddCertTypeToRequestWStr","AddCertTypeToRequestWStr method [Security]","AddCertTypeToRequestWStr method [Security]","IEnroll interface","IEnroll interface [Security]","AddCertTypeToRequestWStr method","IEnroll.AddCertTypeToRequestWStr","IEnroll::AddCertTypeToRequestWStr","security.ienroll4_addcerttypetorequestwstr","xenroll/IEnroll::AddCertTypeToRequestWStr"]
old-location: security\ienroll4_addcerttypetorequestwstr.htm
tech.root: security
ms.assetid: d9bf51db-375e-4230-953c-d9893228d7e1
ms.date: 12/05/2018
ms.keywords: AddCertTypeToRequestWStr, AddCertTypeToRequestWStr method [Security], AddCertTypeToRequestWStr method [Security],IEnroll interface, IEnroll interface [Security],AddCertTypeToRequestWStr method, IEnroll.AddCertTypeToRequestWStr, IEnroll::AddCertTypeToRequestWStr, security.ienroll4_addcerttypetorequestwstr, xenroll/IEnroll::AddCertTypeToRequestWStr
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
 - IEnroll::AddCertTypeToRequestWStr
 - xenroll/IEnroll::AddCertTypeToRequestWStr
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
 - IEnroll.AddCertTypeToRequestWStr
---

# IEnroll::AddCertTypeToRequestWStr


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>AddCertTypeToRequestWStr</b> method adds a certificate template to a request (used to support the enterprise <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA)). This method was first defined by the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll2">IEnroll2</a> interface.

The <b>AddCertTypeToRequestWStr</b> method is an advanced topic that is associated with the Microsoft Certificate Services enterprise Policy Module. Its use is not recommended for most applications.

The phrase "certificate type" is synonymous with "certificate template."

## -parameters

### -param szw [in]

Fully qualified name of the certificate template which is being added to the <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>. This value is interpreted by the certification authority.

## -returns

The return value is an <b>HRESULT</b>, with S_OK returned if the call is successful.

## -remarks

This method can be called multiple times if more than one certificate template is desired for the request.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll</a>