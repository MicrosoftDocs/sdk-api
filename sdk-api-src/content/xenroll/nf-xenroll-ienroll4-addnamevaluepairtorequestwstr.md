---
UID: NF:xenroll.IEnroll4.addNameValuePairToRequestWStr
title: IEnroll4::addNameValuePairToRequestWStr (xenroll.h)
description: Adds an unauthenticated name-value string pair to the request.
helpviewer_keywords: ["IEnroll interface [Security]","addNameValuePairToRequestWStr method","IEnroll4 interface [Security]","addNameValuePairToRequestWStr method","IEnroll4.addNameValuePairToRequestWStr","IEnroll4::addNameValuePairToRequestWStr","IEnroll::addNameValuePairToRequestWStr","addNameValuePairToRequestWStr","addNameValuePairToRequestWStr method [Security]","addNameValuePairToRequestWStr method [Security]","IEnroll interface","addNameValuePairToRequestWStr method [Security]","IEnroll4 interface","security.ienroll4_addnamevaluepairtorequestwstr","xenroll/IEnroll4::addNameValuePairToRequestWStr","xenroll/IEnroll::addNameValuePairToRequestWStr"]
old-location: security\ienroll4_addnamevaluepairtorequestwstr.htm
tech.root: security
ms.assetid: 25f8ae01-e975-4ada-b17c-c97385dc0585
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],addNameValuePairToRequestWStr method, IEnroll4 interface [Security],addNameValuePairToRequestWStr method, IEnroll4.addNameValuePairToRequestWStr, IEnroll4::addNameValuePairToRequestWStr, IEnroll::addNameValuePairToRequestWStr, addNameValuePairToRequestWStr, addNameValuePairToRequestWStr method [Security], addNameValuePairToRequestWStr method [Security],IEnroll interface, addNameValuePairToRequestWStr method [Security],IEnroll4 interface, security.ienroll4_addnamevaluepairtorequestwstr, xenroll/IEnroll4::addNameValuePairToRequestWStr, xenroll/IEnroll::addNameValuePairToRequestWStr
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
 - IEnroll4::addNameValuePairToRequestWStr
 - xenroll/IEnroll4::addNameValuePairToRequestWStr
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
 - IEnroll.addNameValuePairToRequestWStr
 - IEnroll4.addNameValuePairToRequestWStr
---

# IEnroll4::addNameValuePairToRequestWStr


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>addNameValuePairToRequestWStr</b> method adds an unauthenticated name-value string pair to the request. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a> interface.

## -parameters

### -param Flags [in]

This parameter is reserved for future use and must be set to zero.

### -param pwszName [in]

A pointer to a null-terminated wide character string that represents the name portion of the name-value pair.

### -param pwszValue [in]

A pointer to a null-terminated wide character string that represents the value portion of the name-value pair.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll</a>



<b>IEnroll4</b>