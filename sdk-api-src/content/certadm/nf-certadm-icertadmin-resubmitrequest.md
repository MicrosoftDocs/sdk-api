---
UID: NF:certadm.ICertAdmin.ResubmitRequest
title: ICertAdmin::ResubmitRequest (certadm.h)
description: Submits the specified certificate request to the policy module for the specified certification authority. This method was first introduced in the ICertAdmin interface.
helpviewer_keywords: ["CCertAdmin object [Security]","ResubmitRequest method","ICertAdmin interface [Security]","ResubmitRequest method","ICertAdmin.ResubmitRequest","ICertAdmin2 interface [Security]","ResubmitRequest method","ICertAdmin2::ResubmitRequest","ICertAdmin::ResubmitRequest","ResubmitRequest","ResubmitRequest method [Security]","ResubmitRequest method [Security]","CCertAdmin object","ResubmitRequest method [Security]","ICertAdmin interface","ResubmitRequest method [Security]","ICertAdmin2 interface","certadm/ICertAdmin2::ResubmitRequest","certadm/ICertAdmin::ResubmitRequest","security.icertadmin2_resubmitrequest"]
old-location: security\icertadmin2_resubmitrequest.htm
tech.root: security
ms.assetid: 610712d9-3661-42ba-9d2f-27862ba8dbd4
ms.date: 12/05/2018
ms.keywords: CCertAdmin object [Security],ResubmitRequest method, ICertAdmin interface [Security],ResubmitRequest method, ICertAdmin.ResubmitRequest, ICertAdmin2 interface [Security],ResubmitRequest method, ICertAdmin2::ResubmitRequest, ICertAdmin::ResubmitRequest, ResubmitRequest, ResubmitRequest method [Security], ResubmitRequest method [Security],CCertAdmin object, ResubmitRequest method [Security],ICertAdmin interface, ResubmitRequest method [Security],ICertAdmin2 interface, certadm/ICertAdmin2::ResubmitRequest, certadm/ICertAdmin::ResubmitRequest, security.icertadmin2_resubmitrequest
req.header: certadm.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.dll: Certadm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertAdmin::ResubmitRequest
 - certadm/ICertAdmin::ResubmitRequest
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - ICertAdmin2.ResubmitRequest
 - ICertAdmin.ResubmitRequest
 - CCertAdmin.ResubmitRequest
---

# ICertAdmin::ResubmitRequest


## -description

The <b>ResubmitRequest</b> method submits the specified <a href="/windows/desktop/SecGloss/c-gly">certificate request</a> to the 
<a href="/windows/desktop/SecCrypto/policy-modules">policy module</a> for the specified <a href="/windows/desktop/SecGloss/c-gly">certification authority</a>. This method was first introduced in the <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a> interface.

For this method to succeed, the certificate request must be pending.

## -parameters

### -param strConfig [in]

Represents a valid configuration string for the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the network name of the Certificate Services server and CANAME is the common name of the certification authority, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>.

<div class="alert"><b>Important</b>  <b>ResubmitRequest</b> does not clear the internal cache when the configuration string is changed. When you change the configuration string for the CA, you must instantiate a new <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin</a> object and call this method again with the new configuration string.</div>
<div> </div>

### -param RequestId [in]

Specifies the ID of the request to resubmit.

### -param pDisposition [out, retval]

A pointer to the disposition of the request.

## -returns

<h3>C++</h3>
 If the method succeeds and the <i>pDisposition</i> parameter is set to one of the following values that specify the disposition of the request, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value specifies the disposition of the request. This value is one of the following values.

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
The request was not completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The request failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The request was denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_ISSUED</b></dt>
</dl>
</td>
<td width="60%">
The certificate was issued.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_ISSUED_OUT_OF_BAND</b></dt>
</dl>
</td>
<td width="60%">
The certificate was issued separately.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_UNDER_SUBMISSION</b></dt>
</dl>
</td>
<td width="60%">
The request was taken under submission.

</td>
</tr>
</table>

## -remarks

Administration tasks use DCOM. Code that calls this interface method as defined in an earlier version of Certadm.h will run on Windows-based servers as long as the client and the server are both running the same Windows operating system.


#### Examples


```cpp
#include <windows.h>
#include <stdio.h>
#include <Certadm.h>


    long nDisp;  // disposition value
    long nReqID = <REQUESTIDHERE>;
    BSTR bstrCA = NULL;

    bstrCA = SysAllocString(L"<COMPUTERNAMEHERE>\\<CANAMEHERE>");
    if (NULL == bstrCA)
    {
        printf("Memory allocation failed\n");
        goto error;
    }

    //  pCertAdmin is a previously instantiated ICertAdmin object.
    hr = pCertAdmin->ResubmitRequest(bstrCA, nReqID, &nDisp);
    if (FAILED(hr))
    {
        printf("Failed ResubmitRequest [%x]\n", hr);
        goto error;
    }
    else
        printf("ResubmitRequest disposition is %d\n", nDisp);

error:
    //  Free resources.
    if (bstrCA)
        SysFreeString(bstrCA);

```

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">CCertAdmin</a>



<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a>



<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin2</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>



<a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-submit">ICertRequest::Submit</a>