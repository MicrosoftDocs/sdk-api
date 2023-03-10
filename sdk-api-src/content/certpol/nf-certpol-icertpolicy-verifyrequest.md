---
UID: NF:certpol.ICertPolicy.VerifyRequest
title: ICertPolicy::VerifyRequest (certpol.h)
description: Notifies the policy module that a new request has entered the system.
helpviewer_keywords: ["CCertPolicy object [Security]","VerifyRequest method","ICertPolicy interface [Security]","VerifyRequest method","ICertPolicy.VerifyRequest","ICertPolicy2 interface [Security]","VerifyRequest method","ICertPolicy2::VerifyRequest","ICertPolicy::VerifyRequest","VR_INSTANT_BAD","VR_INSTANT_OK","VR_PENDING","VerifyRequest","VerifyRequest method [Security]","VerifyRequest method [Security]","CCertPolicy object","VerifyRequest method [Security]","ICertPolicy interface","VerifyRequest method [Security]","ICertPolicy2 interface","_certsrv_icertpolicy_verifyrequest","certpol/ICertPolicy2::VerifyRequest","certpol/ICertPolicy::VerifyRequest","security.icertpolicy2_verifyrequest"]
old-location: security\icertpolicy2_verifyrequest.htm
tech.root: security
ms.assetid: 860f0eb0-5b23-44bd-8416-687a94962f1b
ms.date: 12/05/2018
ms.keywords: CCertPolicy object [Security],VerifyRequest method, ICertPolicy interface [Security],VerifyRequest method, ICertPolicy.VerifyRequest, ICertPolicy2 interface [Security],VerifyRequest method, ICertPolicy2::VerifyRequest, ICertPolicy::VerifyRequest, VR_INSTANT_BAD, VR_INSTANT_OK, VR_PENDING, VerifyRequest, VerifyRequest method [Security], VerifyRequest method [Security],CCertPolicy object, VerifyRequest method [Security],ICertPolicy interface, VerifyRequest method [Security],ICertPolicy2 interface, _certsrv_icertpolicy_verifyrequest, certpol/ICertPolicy2::VerifyRequest, certpol/ICertPolicy::VerifyRequest, security.icertpolicy2_verifyrequest
req.header: certpol.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertPolicy::VerifyRequest
 - certpol/ICertPolicy::VerifyRequest
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certidl.lib
 - Certidl.dll
api_name:
 - ICertPolicy2.VerifyRequest
 - ICertPolicy.VerifyRequest
 - CCertPolicy.VerifyRequest
---

# ICertPolicy::VerifyRequest


## -description

The <b>VerifyRequest</b> method notifies the policy module that a new request has entered the system. The policy module can then interact with that request by passing <i>Context</i> as a parameter when retrieving or setting properties on the request or associated certificate.

The returned disposition value indicates whether the request has been accepted, denied, or has been sent to the administration queue for later evaluation.

## -parameters

### -param strConfig [in]

Represents the name of the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a>, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>.

### -param Context [in]

Identifies the request and associated certificate under construction. The certificate server passes the context to this method.

### -param bNewRequest [in]

If set to <b>TRUE</b>, specifies that the request is new. If set to <b>FALSE</b>, the request is being resubmitted to the policy module as a result of an 
<a href="/windows/desktop/api/certadm/nf-certadm-icertadmin-resubmitrequest">ICertAdmin::ResubmitRequest</a> call. A value of <b>FALSE</b> can be used to indicate that the administrator wants the request to be issued or that request properties set by the administrator should be examined.

Note that <b>TRUE</b> is defined (in a Microsoft header file) for C/C++ programmers as one, while  Visual Basic defines the <b>True</b> keyword as negative one. As a result, Visual Basic developers must use one (instead of <b>True</b>) to set this parameter to <b>TRUE</b>. However, to set this parameter to <b>FALSE</b>, Visual Basic developers can use zero or <b>False</b>.

### -param Flags [in]

This parameter is reserved and must be set to zero.

### -param pDisposition [out, retval]

A pointer to the disposition value. The method sets one of the following dispositions.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VR_INSTANT_BAD"></a><a id="vr_instant_bad"></a><dl>
<dt><b>VR_INSTANT_BAD</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Deny the request.

</td>
</tr>
<tr>
<td width="40%"><a id="VR_INSTANT_OK"></a><a id="vr_instant_ok"></a><dl>
<dt><b>VR_INSTANT_OK</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Accept the request.

</td>
</tr>
<tr>
<td width="40%"><a id="VR_PENDING"></a><a id="vr_pending"></a><dl>
<dt><b>VR_PENDING</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Add the request to the queue to accept or deny the request at a later  time.

</td>
</tr>
</table>

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
The return value specifies the disposition, which must be one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VR_INSTANT_BAD</b></dt>
</dl>
</td>
<td width="60%">
Deny the request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VR_INSTANT_OK</b></dt>
</dl>
</td>
<td width="60%">
Accept the request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VR_PENDING</b></dt>
</dl>
</td>
<td width="60%">
Add the request to the queue to accept or deny the request at a later  time.

</td>
</tr>
</table>

## -remarks

<b>VerifyRequest</b> is free to spawn off other processes or access an external database to do the request verification. If the verification requires out-of-band processing or human intervention, <b>VerifyRequest</b> can notify another process or leave any notice of the incoming request required. After the out-of-band processing is complete, a call to 
<a href="/windows/desktop/api/certadm/nf-certadm-icertadmin-resubmitrequest">ResubmitRequest</a> can be made, or the provided administration tool can be used to resubmit the request to the Policy Module. The policy module can examine the request again, access any necessary external data, and return a value to indicate the certificate should be issued or denied.

When you write custom policy modules, you must implement <b>VerifyRequest</b> functionality in your modules.


#### Examples

The following example shows a possible implementation of the <b>VerifyRequest</b> method.


```cpp
#include <windows.h>
#include <stdio.h>
#include <Certpol.h>

STDMETHODIMP CCertPolicy::VerifyRequest(
             BSTR const strConfig,
             LONG Context,
             LONG bNewRequest,
             LONG Flags,
             LONG __RPC_FAR *pDisposition)
{
    HRESULT            hr;
    long               nDisp = VR_INSTANT_BAD;
    ICertServerPolicy *pServer = NULL;
    BSTR               bstrPropName = NULL;
    VARIANT            varProp;

    // Verify that pointer is not NULL.
    if ( NULL == pDisposition )
    {
        hr = E_POINTER;  // E_POINTER is #defined in Winerror.h
        goto error;
    }
    
    // Set disposition to pending.
    *pDisposition = VR_PENDING; 

    // Obtain a pointer to the CertServerPolicy interface.
    hr = CoCreateInstance( CLSID_CCertServerPolicy,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ICertServerPolicy,
                           (void **) &pServer);
    if (FAILED( hr ))
    {
        printf("Failed CoCreateInstance for pServer - %x\n", hr );
        goto error;
    }

    // Set the context to refer to this request.
    hr = pServer->SetContext(Context);
    if (FAILED( hr ))
    {
        printf("Failed SetContext(%u) - %x\n", Context, hr );
        goto error;
    }

    // This policy will perform a database check on the CN.
    // Set the property name to Subject.Commonname.
    bstrPropName = SysAllocString(L"Subject.Commonname");
    if ( NULL == bstrPropName )
    {
        hr = E_OUTOFMEMORY;  // #defined in Winerror.h
        printf("Failed SysAllocString (no memory)\n" );
        goto error;
    }

    // Retrieve the certificate property for the CN.
    // Actual implementations may want to examine other properties.
    VariantInit( &varProp );
    hr = pServer->GetCertificateProperty( bstrPropName,
                                          PROPTYPE_STRING,
                                          &varProp );
    if (FAILED(hr))
    {
        printf("Failed GetCertificateProperty - %x\n", hr);
        goto error;
    }

    // For this simple sample, merely check CN in a database.
    // (Implementation not shown, as it is application-specific).
    hr = MyDatabaseCheck( varProp.bstrVal );
    if ( S_OK == hr )
        *pDisposition = VR_INSTANT_OK;   // Accepted.
    else 
        *pDisposition = VR_INSTANT_BAD;  // Denied.

error:

    // Free resources.
    if (NULL != pServer)
        pServer->Release();

    VariantClear( &varProp );

    if ( NULL != bstrPropName )
        SysFreeString( bstrPropName );

    return(hr);
}
```

## -see-also

<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>



<a href="/windows/desktop/api/certpol/nn-certpol-icertpolicy">ICertPolicy</a>



<a href="/windows/desktop/api/certpol/nn-certpol-icertpolicy2">ICertPolicy2</a>