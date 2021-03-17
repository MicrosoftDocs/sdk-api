---
UID: NF:certcli.ICertRequest.GetRequestId
title: ICertRequest::GetRequestId (certcli.h)
description: Gets the current internal request number for the request and subsequent certificate.
helpviewer_keywords: ["CCertRequest object [Security]","GetRequestId method","GetRequestId","GetRequestId method [Security]","GetRequestId method [Security]","CCertRequest object","GetRequestId method [Security]","ICertRequest interface","GetRequestId method [Security]","ICertRequest2 interface","GetRequestId method [Security]","ICertRequest3 interface","ICertRequest interface [Security]","GetRequestId method","ICertRequest.GetRequestId","ICertRequest2 interface [Security]","GetRequestId method","ICertRequest2::GetRequestId","ICertRequest3 interface [Security]","GetRequestId method","ICertRequest3::GetRequestId","ICertRequest::GetRequestId","certcli/ICertRequest2::GetRequestId","certcli/ICertRequest3::GetRequestId","certcli/ICertRequest::GetRequestId","security.icertrequest2_getrequestid"]
old-location: security\icertrequest2_getrequestid.htm
tech.root: security
ms.assetid: bb808834-7083-4b14-bce7-96b6fef242cc
ms.date: 12/05/2018
ms.keywords: CCertRequest object [Security],GetRequestId method, GetRequestId, GetRequestId method [Security], GetRequestId method [Security],CCertRequest object, GetRequestId method [Security],ICertRequest interface, GetRequestId method [Security],ICertRequest2 interface, GetRequestId method [Security],ICertRequest3 interface, ICertRequest interface [Security],GetRequestId method, ICertRequest.GetRequestId, ICertRequest2 interface [Security],GetRequestId method, ICertRequest2::GetRequestId, ICertRequest3 interface [Security],GetRequestId method, ICertRequest3::GetRequestId, ICertRequest::GetRequestId, certcli/ICertRequest2::GetRequestId, certcli/ICertRequest3::GetRequestId, certcli/ICertRequest::GetRequestId, security.icertrequest2_getrequestid
req.header: certcli.h
req.include-header: Certsrv.h
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
req.lib: Certidl.lib
req.dll: Certcli.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertRequest::GetRequestId
 - certcli/ICertRequest::GetRequestId
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
 - ICertRequest3.GetRequestId
 - ICertRequest2.GetRequestId
 - ICertRequest.GetRequestId
 - CCertRequest.GetRequestId
---

# ICertRequest::GetRequestId


## -description

The <b>GetRequestId</b> method gets the current internal request number for the request and subsequent certificate.

This can be used to reference a request unambiguously to a server administrator or other interface.

## -parameters

### -param pRequestId [out]

A pointer to the request ID value.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

Upon successful completion of this function, *<i>pRequestId</i> is set to the value of the request ID.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value specifies the current internal request number for the request and subsequent certificate.

## -see-also

<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest">CCertRequest</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest">ICertRequest</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest2">ICertRequest2</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest3">ICertRequest3</a>