---
UID: NF:certcli.ICertRequest.RetrievePending
title: ICertRequest::RetrievePending (certcli.h)
description: Retrieves a certificate's disposition status from an earlier request that may have previously returned CR_DISP_INCOMPLETE or CR_DISP_UNDER_SUBMISSION.
helpviewer_keywords: ["CCertRequest object [Security]","RetrievePending method","ICertRequest interface [Security]","RetrievePending method","ICertRequest.RetrievePending","ICertRequest2 interface [Security]","RetrievePending method","ICertRequest2::RetrievePending","ICertRequest3 interface [Security]","RetrievePending method","ICertRequest3::RetrievePending","ICertRequest::RetrievePending","RetrievePending","RetrievePending method [Security]","RetrievePending method [Security]","CCertRequest object","RetrievePending method [Security]","ICertRequest interface","RetrievePending method [Security]","ICertRequest2 interface","RetrievePending method [Security]","ICertRequest3 interface","certcli/ICertRequest2::RetrievePending","certcli/ICertRequest3::RetrievePending","certcli/ICertRequest::RetrievePending","security.icertrequest2_retrievepending"]
old-location: security\icertrequest2_retrievepending.htm
tech.root: security
ms.assetid: 07a9ac57-f90e-4c5c-b563-8aebbcf8f42e
ms.date: 12/05/2018
ms.keywords: CCertRequest object [Security],RetrievePending method, ICertRequest interface [Security],RetrievePending method, ICertRequest.RetrievePending, ICertRequest2 interface [Security],RetrievePending method, ICertRequest2::RetrievePending, ICertRequest3 interface [Security],RetrievePending method, ICertRequest3::RetrievePending, ICertRequest::RetrievePending, RetrievePending, RetrievePending method [Security], RetrievePending method [Security],CCertRequest object, RetrievePending method [Security],ICertRequest interface, RetrievePending method [Security],ICertRequest2 interface, RetrievePending method [Security],ICertRequest3 interface, certcli/ICertRequest2::RetrievePending, certcli/ICertRequest3::RetrievePending, certcli/ICertRequest::RetrievePending, security.icertrequest2_retrievepending
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
 - ICertRequest::RetrievePending
 - certcli/ICertRequest::RetrievePending
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
 - ICertRequest3.RetrievePending
 - ICertRequest2.RetrievePending
 - ICertRequest.RetrievePending
 - CCertRequest.RetrievePending
---

# ICertRequest::RetrievePending


## -description

The <b>RetrievePending</b> method retrieves a certificate's disposition status from an earlier request that may have previously returned CR_DISP_INCOMPLETE or CR_DISP_UNDER_SUBMISSION.

If the resulting disposition status is CR_DISP_ISSUED, you can retrieve the issued certificate by calling 
<a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-getcertificate">ICertRequest3::GetCertificate</a>. If a disposition other than CR_DISP_ISSUED is returned, call 
<a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-getlaststatus">ICertRequest3::GetLastStatus</a>, 
<a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-getdispositionmessage">ICertRequest3::GetDispositionMessage</a>, or both methods for more information.

## -parameters

### -param RequestId [in]

The ID of the request that had previously returned CR_DISP_INCOMPLETE or CR_DISP_UNDER_SUBMISSION.

### -param strConfig [in]

Represents a valid configuration string for the Certificate Services server. The string can be either an HTTPS URL for an enrollment server or in the form <i>ComputerName</i><b>\\</b><i>CAName</i>, where <i>ComputerName</i> is the network name of the server, and <i>CAName</i> is the common name of the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a>, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>An HTTPS URL is not supported as an input.

### -param pDisposition [out, retval]

A pointer to the request's disposition value.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

Upon successful completion of this function, *<i>pDisposition</i> is set to one of the values in the following table.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value specifies the disposition of the request. The disposition is one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_INCOMPLETE</b></dt>
</dl>
</td>
<td width="60%">
Request did not complete

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Request failed

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Request denied

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_ISSUED</b></dt>
</dl>
</td>
<td width="60%">
Certificate issued

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_ISSUED_OUT_OF_BAND</b></dt>
</dl>
</td>
<td width="60%">
Certificate issued separately

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_UNDER_SUBMISSION</b></dt>
</dl>
</td>
<td width="60%">
Request taken under submission

</td>
</tr>
</table>

## -remarks

A successful call to this method generates an EXITEVENT_CERTRETRIEVEPENDING event. An active exit module will receive notification of this event (by means of a call to 
<a href="/windows/desktop/api/certexit/nf-certexit-icertexit-notify">ICertExit3::Notify</a>) if the exit module specified this event when calling 
<a href="/windows/desktop/api/certexit/nf-certexit-icertexit-initialize">ICertExit3::Initialize</a>.


#### Examples


```cpp
BSTR    bstrCA = NULL;
long    nReqID, nDisp;

// In this example, the request ID is hard-coded.
nReqID = 1234;

// Note use of two '\' in C++ to produce one '\'.
bstrCA = SysAllocString(L"server01\\myCAName");

// pCertRequest is previously instantiated ICertRequest
// object pointer. Retrieve the status for the specified request.
hr = pCertRequest->RetrievePending( nReqID, bstrCA, &nDisp );
if (FAILED(hr))
{
    printf("Failed RetrievePending [%x]\n", hr);
    goto error;
}
else
{
    // Use the disposition value as needed...
}
// Free BSTR resource.
if ( NULL != bstrCA )
    SysFreeString( bstrCA );
```

## -see-also

<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest">CCertRequest</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest">ICertRequest</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest2">ICertRequest2</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest3">ICertRequest3</a>