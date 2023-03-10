---
UID: NF:certcli.ICertRequest3.GetRequestIdString
title: ICertRequest3::GetRequestIdString (certcli.h)
description: Gets the current internal request number, formatted as a string, for the request and subsequent certificate.
helpviewer_keywords: ["CCertRequest object [Security]","GetRequestIdString method","GetRequestIdString","GetRequestIdString method [Security]","GetRequestIdString method [Security]","CCertRequest object","GetRequestIdString method [Security]","ICertRequest3 class","ICertRequest3 class [Security]","GetRequestIdString method","ICertRequest3.GetRequestIdString","ICertRequest3::GetRequestIdString","certcli/ICertRequest3::GetRequestIdString","security.icertrequest3_getrequestidstring"]
old-location: security\icertrequest3_getrequestidstring.htm
tech.root: security
ms.assetid: 09afc06f-95e8-4519-b0c7-36da5986e077
ms.date: 12/05/2018
ms.keywords: CCertRequest object [Security],GetRequestIdString method, GetRequestIdString, GetRequestIdString method [Security], GetRequestIdString method [Security],CCertRequest object, GetRequestIdString method [Security],ICertRequest3 class, ICertRequest3 class [Security],GetRequestIdString method, ICertRequest3.GetRequestIdString, ICertRequest3::GetRequestIdString, certcli/ICertRequest3::GetRequestIdString, security.icertrequest3_getrequestidstring
req.header: certcli.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certidl.lib
req.dll: Certcli.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertRequest3::GetRequestIdString
 - certcli/ICertRequest3::GetRequestIdString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certcli.dll
api_name:
 - ICertRequest3.GetRequestIdString
 - CCertRequest.GetRequestIdString
---

# ICertRequest3::GetRequestIdString


## -description

The <b>GetRequestIdString</b> method gets the current internal request number, formatted as a string, for the request and subsequent certificate.

This can be used to reference a request unambiguously to a server administrator or other interface.

## -parameters

### -param pstrRequestId [out, retval]

A pointer to <b>BSTR</b> variable to receive the request ID string.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns <b>S_OK</b>.

Upon successful completion of this function, the string pointed to by the <i>pstrRequestId</i> parameter is set to the request ID string.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value specifies the current internal request number, as a string, for the request and subsequent certificate.

## -see-also

<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest">CCertRequest</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest3">ICertRequest3</a>