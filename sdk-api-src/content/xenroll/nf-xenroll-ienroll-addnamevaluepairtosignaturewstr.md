---
UID: NF:xenroll.IEnroll.AddNameValuePairToSignatureWStr
title: IEnroll::AddNameValuePairToSignatureWStr (xenroll.h)
description: Adds the authenticated name-value pair of an attribute to the request. The certification authority (CA) interprets the meaning of the name-value pair.
helpviewer_keywords: ["AddNameValuePairToSignatureWStr","AddNameValuePairToSignatureWStr method [Security]","AddNameValuePairToSignatureWStr method [Security]","IEnroll interface","AddNameValuePairToSignatureWStr method [Security]","IEnroll4 interface","IEnroll interface [Security]","AddNameValuePairToSignatureWStr method","IEnroll.AddNameValuePairToSignatureWStr","IEnroll4 interface [Security]","AddNameValuePairToSignatureWStr method","IEnroll4::AddNameValuePairToSignatureWStr","IEnroll::AddNameValuePairToSignatureWStr","security.ienroll4_addnamevaluepairtosignaturewstr","xenroll/IEnroll4::AddNameValuePairToSignatureWStr","xenroll/IEnroll::AddNameValuePairToSignatureWStr"]
old-location: security\ienroll4_addnamevaluepairtosignaturewstr.htm
tech.root: security
ms.assetid: 8ccc0bdf-01db-4863-aaaf-94910bfa0b8b
ms.date: 12/05/2018
ms.keywords: AddNameValuePairToSignatureWStr, AddNameValuePairToSignatureWStr method [Security], AddNameValuePairToSignatureWStr method [Security],IEnroll interface, AddNameValuePairToSignatureWStr method [Security],IEnroll4 interface, IEnroll interface [Security],AddNameValuePairToSignatureWStr method, IEnroll.AddNameValuePairToSignatureWStr, IEnroll4 interface [Security],AddNameValuePairToSignatureWStr method, IEnroll4::AddNameValuePairToSignatureWStr, IEnroll::AddNameValuePairToSignatureWStr, security.ienroll4_addnamevaluepairtosignaturewstr, xenroll/IEnroll4::AddNameValuePairToSignatureWStr, xenroll/IEnroll::AddNameValuePairToSignatureWStr
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
 - IEnroll::AddNameValuePairToSignatureWStr
 - xenroll/IEnroll::AddNameValuePairToSignatureWStr
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
 - IEnroll.AddNameValuePairToSignatureWStr
 - IEnroll4.AddNameValuePairToSignatureWStr
---

# IEnroll::AddNameValuePairToSignatureWStr


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>AddNameValuePairToSignatureWStr</b> method adds the authenticated name-value pair of an <a href="/windows/desktop/SecGloss/a-gly">attribute</a> to the request. The <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) interprets the meaning of the name-value pair.
		 This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll2">IEnroll2</a> interface.

## -parameters

### -param Name [in]

A null-terminated Unicode string that contains the name of the attribute, such as "2.5.4.6", for the country/region name.

### -param Value [in]

 A null-terminated Unicode string that contains the value of the attribute, such as "US" or "<i>DomainName</i>&#92;<i>UserID</i>".

## -returns

The return value is an <b>HRESULT</b>, with S_OK returned if the call is successful.

## -remarks

The <b>AddNameValuePairToSignatureWStr</b> method is used  to add attributes to the request.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll</a>



<b>IEnroll4</b>