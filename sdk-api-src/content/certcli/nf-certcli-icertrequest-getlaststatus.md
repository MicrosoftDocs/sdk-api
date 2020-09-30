---
UID: NF:certcli.ICertRequest.GetLastStatus
title: ICertRequest::GetLastStatus (certcli.h)
description: Gets the last return code for this request. This returns the error code information, rather than the disposition of the request.
helpviewer_keywords: ["CCertRequest object [Security]","GetLastStatus method","GetLastStatus","GetLastStatus method [Security]","GetLastStatus method [Security]","CCertRequest object","GetLastStatus method [Security]","ICertRequest interface","GetLastStatus method [Security]","ICertRequest2 interface","GetLastStatus method [Security]","ICertRequest3 interface","ICertRequest interface [Security]","GetLastStatus method","ICertRequest.GetLastStatus","ICertRequest2 interface [Security]","GetLastStatus method","ICertRequest2::GetLastStatus","ICertRequest3 interface [Security]","GetLastStatus method","ICertRequest3::GetLastStatus","ICertRequest::GetLastStatus","certcli/ICertRequest2::GetLastStatus","certcli/ICertRequest3::GetLastStatus","certcli/ICertRequest::GetLastStatus","security.icertrequest2_getlaststatus"]
old-location: security\icertrequest2_getlaststatus.htm
tech.root: security
ms.assetid: ebe5cfa7-6bfd-4454-9272-64e3b1bf0ae2
ms.date: 12/05/2018
ms.keywords: CCertRequest object [Security],GetLastStatus method, GetLastStatus, GetLastStatus method [Security], GetLastStatus method [Security],CCertRequest object, GetLastStatus method [Security],ICertRequest interface, GetLastStatus method [Security],ICertRequest2 interface, GetLastStatus method [Security],ICertRequest3 interface, ICertRequest interface [Security],GetLastStatus method, ICertRequest.GetLastStatus, ICertRequest2 interface [Security],GetLastStatus method, ICertRequest2::GetLastStatus, ICertRequest3 interface [Security],GetLastStatus method, ICertRequest3::GetLastStatus, ICertRequest::GetLastStatus, certcli/ICertRequest2::GetLastStatus, certcli/ICertRequest3::GetLastStatus, certcli/ICertRequest::GetLastStatus, security.icertrequest2_getlaststatus
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
 - ICertRequest::GetLastStatus
 - certcli/ICertRequest::GetLastStatus
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
 - ICertRequest3.GetLastStatus
 - ICertRequest2.GetLastStatus
 - ICertRequest.GetLastStatus
 - CCertRequest.GetLastStatus
---

# ICertRequest::GetLastStatus


## -description

The <b>GetLastStatus</b> method gets the last return code for this request. This returns the error code information, rather than the disposition of the request.

## -parameters

### -param pStatus [out]

A pointer to the request's status code.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

Upon successful completion of this function, *<i>pStatus</i> is set to the result code of the latest call to <a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-submit">ICertRequest3::Submit</a>, <a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-retrievepending">ICertRequest3::RetrievePending</a>, or <a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-getcacertificate">ICertRequest3::GetCACertificate</a>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the result code of the latest call to <a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-submit">CCertRequest3.Submit</a>, <a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-retrievepending">CCertRequest3.RetrievePending</a> or <a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-getcacertificate">CCertRequest3.GetCACertificate</a>.

## -remarks

The value retrieved by <b>GetLastStatus</b> depends on the most recent call to 
<a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-submit">ICertRequest3::Submit</a>, 
<a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-retrievepending">ICertRequest3::RetrievePending</a>, or 
<a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-getcacertificate">ICertRequest3::GetCACertificate</a>. If a call to one of these methods fails on the server, call <b>GetLastStatus</b> to retrieve the error number. Some server failures (such as denied requests) return S_OK and a disposition other than CR_DISP_ISSUED from the method call, and you can use <b>GetLastStatus</b> to retrieve the specific cause of failure. If a call to one of these methods succeeds, then a subsequent call to <b>GetLastStatus</b> returns S_OK (which is zero).

Additionally, the request disposition is stored in the Certificate Services database, and can be viewed by means of the Certification Authority MMC snap-in (choose the Request Disposition column).


#### Examples


```cpp
HRESULT    hrServer, hr;
// pCertRequest is previously instantiated
// ICertRequest object pointer.
hr = pCertRequest->GetLastStatus((LONG *) &hrServer);
if (FAILED(hr))
{
    printf("Failed GetLastStatus [%x]\n", hr);
    goto error;
}
else
{
    // Use the HRESULT value as needed...
}

```

## -see-also

<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest">CCertRequest</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest">ICertRequest</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest2">ICertRequest2</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest3">ICertRequest3</a>