---
UID: NF:xenroll.ICEnroll4.addNameValuePairToRequest
title: ICEnroll4::addNameValuePairToRequest (xenroll.h)
description: Adds an unauthenticated name-value string pair to the request. This method was first defined in the ICEnroll4 interface.
helpviewer_keywords: ["CEnroll object [Security]","addNameValuePairToRequest method","ICEnroll4 interface [Security]","addNameValuePairToRequest method","ICEnroll4.addNameValuePairToRequest","ICEnroll4::addNameValuePairToRequest","_xen_icenroll4_addnamevaluepairtorequest","addNameValuePairToRequest","addNameValuePairToRequest method [Security]","addNameValuePairToRequest method [Security]","CEnroll object","addNameValuePairToRequest method [Security]","ICEnroll4 interface","security.icenroll4_addnamevaluepairtorequest","xenroll/ICEnroll4::addNameValuePairToRequest"]
old-location: security\icenroll4_addnamevaluepairtorequest.htm
tech.root: security
ms.assetid: 252d1789-1207-4281-b044-e1f1ca6cd585
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],addNameValuePairToRequest method, ICEnroll4 interface [Security],addNameValuePairToRequest method, ICEnroll4.addNameValuePairToRequest, ICEnroll4::addNameValuePairToRequest, _xen_icenroll4_addnamevaluepairtorequest, addNameValuePairToRequest, addNameValuePairToRequest method [Security], addNameValuePairToRequest method [Security],CEnroll object, addNameValuePairToRequest method [Security],ICEnroll4 interface, security.icenroll4_addnamevaluepairtorequest, xenroll/ICEnroll4::addNameValuePairToRequest
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
 - ICEnroll4::addNameValuePairToRequest
 - xenroll/ICEnroll4::addNameValuePairToRequest
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
 - ICEnroll4.addNameValuePairToRequest
 - CEnroll.addNameValuePairToRequest
---

# ICEnroll4::addNameValuePairToRequest


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>addNameValuePairToRequest</b> method adds an unauthenticated name-value string pair to the request. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a> interface.

## -parameters

### -param Flags [in]

This parameter is reserved for future use and must be set to zero.

### -param strName [in]

The name portion of the name-value pair.

### -param strValue [in]

The value portion of the name-value pair.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.