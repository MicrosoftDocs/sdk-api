---
UID: NF:certcli.ICertRequest.GetDispositionMessage
title: ICertRequest::GetDispositionMessage (certcli.h)
description: Gets a human-readable message that gives the current disposition of the certificate request.
helpviewer_keywords: ["CCertRequest object [Security]","GetDispositionMessage method","GetDispositionMessage","GetDispositionMessage method [Security]","GetDispositionMessage method [Security]","CCertRequest object","GetDispositionMessage method [Security]","ICertRequest interface","GetDispositionMessage method [Security]","ICertRequest2 interface","GetDispositionMessage method [Security]","ICertRequest3 interface","ICertRequest interface [Security]","GetDispositionMessage method","ICertRequest.GetDispositionMessage","ICertRequest2 interface [Security]","GetDispositionMessage method","ICertRequest2::GetDispositionMessage","ICertRequest3 interface [Security]","GetDispositionMessage method","ICertRequest3::GetDispositionMessage","ICertRequest::GetDispositionMessage","certcli/ICertRequest2::GetDispositionMessage","certcli/ICertRequest3::GetDispositionMessage","certcli/ICertRequest::GetDispositionMessage","security.icertrequest2_getdispositionmessage"]
old-location: security\icertrequest2_getdispositionmessage.htm
tech.root: security
ms.assetid: c3639cf6-c70f-4f15-a0ed-e60abe2955cb
ms.date: 12/05/2018
ms.keywords: CCertRequest object [Security],GetDispositionMessage method, GetDispositionMessage, GetDispositionMessage method [Security], GetDispositionMessage method [Security],CCertRequest object, GetDispositionMessage method [Security],ICertRequest interface, GetDispositionMessage method [Security],ICertRequest2 interface, GetDispositionMessage method [Security],ICertRequest3 interface, ICertRequest interface [Security],GetDispositionMessage method, ICertRequest.GetDispositionMessage, ICertRequest2 interface [Security],GetDispositionMessage method, ICertRequest2::GetDispositionMessage, ICertRequest3 interface [Security],GetDispositionMessage method, ICertRequest3::GetDispositionMessage, ICertRequest::GetDispositionMessage, certcli/ICertRequest2::GetDispositionMessage, certcli/ICertRequest3::GetDispositionMessage, certcli/ICertRequest::GetDispositionMessage, security.icertrequest2_getdispositionmessage
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
 - ICertRequest::GetDispositionMessage
 - certcli/ICertRequest::GetDispositionMessage
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
 - ICertRequest3.GetDispositionMessage
 - ICertRequest2.GetDispositionMessage
 - ICertRequest.GetDispositionMessage
 - CCertRequest.GetDispositionMessage
---

# ICertRequest::GetDispositionMessage


## -description

The <b>GetDispositionMessage</b> method gets a human-readable message that gives the current disposition of the <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>.

Note that the message returned here may have more detail than the returned error code. For example, 
<a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-getlaststatus">ICertRequest3::GetLastStatus</a> may return an <b>HRESULT</b>, while <b>GetDispositionMessage</b> will return a detailed reason that specifies why the request was denied.

## -parameters

### -param pstrDispositionMessage [out]

A pointer to the <b>BSTR</b> that contains the disposition message.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

Upon successful completion of this function, *<i>pstrDispositionMessage</i> is set to the <b>BSTR</b> that contains a human-readable message that gives the current disposition of the <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>. To use this method, create a variable of <b>BSTR</b> type, set the variable equal to <b>NULL</b>, and pass the address of this variable as <i>pstrDispositionMessage</i>. When you have finished using the <b>BSTR</b>, free it by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a string that contains a human-readable message that gives the current disposition of the <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>.

## -remarks

An application would call this method to obtain the message retrieved from the server by means of an earlier call to 
<a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-submit">ICertRequest3::Submit</a> or 
<a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-retrievepending">ICertRequest3::RetrievePending</a>. Additionally, the message is stored in the Certificate Services database and may be viewed by the Certification Authority MMC snap-in (choose the Request Disposition Message column). If the message contains localized text, it was localized on the server (based on the server's locale).


#### Examples


```cpp
#include <windows.h>
#include <stdio.h>
#include <Certcli.h>

    BSTR    bstrDispMsg = NULL;
    // pCertRequest is previously instantiated ICertRequest object 
    // pointer. Retrieve the disposition message for the 
    // previous request.
    hr = pCertRequest->GetDispositionMessage(&bstrDispMsg);
    if (FAILED(hr))
    {
        printf("Failed GetDispositionMessage [%x]\n", hr);
        goto error;
    }
    else
    {
        // Use the disposition message as needed...
    }

    // Done processing.

error:

    // Free BSTR values.
    if (NULL != bstrCA)
        SysFreeString(bstrCA);

    if (NULL != bstrDispMsg)
        SysFreeString(bstrDispMsg);

```

## -see-also

<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest">CCertRequest</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest">ICertRequest</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest2">ICertRequest2</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest3">ICertRequest3</a>