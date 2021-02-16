---
UID: NF:xenroll.ICEnroll4.addAttributeToRequest
title: ICEnroll4::addAttributeToRequest (xenroll.h)
description: Adds an attribute to the certificate request. This method was first defined in the ICEnroll4 interface.
helpviewer_keywords: ["CEnroll object [Security]","addAttributeToRequest method","ICEnroll4 interface [Security]","addAttributeToRequest method","ICEnroll4.addAttributeToRequest","ICEnroll4::addAttributeToRequest","_xen_icenroll4_addattributetorequest","addAttributeToRequest","addAttributeToRequest method [Security]","addAttributeToRequest method [Security]","CEnroll object","addAttributeToRequest method [Security]","ICEnroll4 interface","security.icenroll4_addattributetorequest","xenroll/ICEnroll4::addAttributeToRequest"]
old-location: security\icenroll4_addattributetorequest.htm
tech.root: security
ms.assetid: a15fe06c-e2a5-4292-ad82-ea350e652a07
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],addAttributeToRequest method, ICEnroll4 interface [Security],addAttributeToRequest method, ICEnroll4.addAttributeToRequest, ICEnroll4::addAttributeToRequest, _xen_icenroll4_addattributetorequest, addAttributeToRequest, addAttributeToRequest method [Security], addAttributeToRequest method [Security],CEnroll object, addAttributeToRequest method [Security],ICEnroll4 interface, security.icenroll4_addattributetorequest, xenroll/ICEnroll4::addAttributeToRequest
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
 - ICEnroll4::addAttributeToRequest
 - xenroll/ICEnroll4::addAttributeToRequest
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
 - ICEnroll4.addAttributeToRequest
 - CEnroll.addAttributeToRequest
---

# ICEnroll4::addAttributeToRequest


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>addAttributeToRequest</b> method adds an <a href="/windows/desktop/SecGloss/a-gly">attribute</a> to the <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>.  This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a> interface.

## -parameters

### -param Flags [in]

This parameter is reserved for future use and must be set to zero.

### -param strName [in]

An <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) that represents the attribute name.

### -param strValue [in]

A base64-encoded or binary attribute value.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.