---
UID: NF:xenroll.ICEnroll4.createRequest
title: ICEnroll4::createRequest (xenroll.h)
description: Creates a PKCS (ICEnroll4.createRequest)
helpviewer_keywords: ["CEnroll object [Security]","createRequest method","ICEnroll4 interface [Security]","createRequest method","ICEnroll4.createRequest","ICEnroll4::createRequest","XECR_CMC","XECR_PKCS10_V1_5","XECR_PKCS10_V2_0","XECR_PKCS7","_xen_icenroll4_createrequest","createRequest","createRequest method [Security]","createRequest method [Security]","CEnroll object","createRequest method [Security]","ICEnroll4 interface","security.icenroll4_createrequest","xenroll/ICEnroll4::createRequest"]
old-location: security\icenroll4_createrequest.htm
tech.root: security
ms.assetid: d2a1c1c4-dbbf-423c-bf59-da0ab9a71078
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],createRequest method, ICEnroll4 interface [Security],createRequest method, ICEnroll4.createRequest, ICEnroll4::createRequest, XECR_CMC, XECR_PKCS10_V1_5, XECR_PKCS10_V2_0, XECR_PKCS7, _xen_icenroll4_createrequest, createRequest, createRequest method [Security], createRequest method [Security],CEnroll object, createRequest method [Security],ICEnroll4 interface, security.icenroll4_createrequest, xenroll/ICEnroll4::createRequest
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
 - ICEnroll4::createRequest
 - xenroll/ICEnroll4::createRequest
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
 - ICEnroll4.createRequest
 - CEnroll.createRequest
---

# ICEnroll4::createRequest


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>createRequest</b> method creates a PKCS #10, <a href="/windows/desktop/SecGloss/p-gly">PKCS #7</a>, or full <a href="/windows/desktop/SecGloss/c-gly">Certificate Management over CMS</a> (CMC) format <a href="/windows/desktop/SecGloss/c-gly">certificate request</a> and stores it in a string. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a> interface.

## -parameters

### -param Flags [in]

A value that specifies the type of certificate request to create. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XECR_CMC"></a><a id="xecr_cmc"></a><dl>
<dt><b>XECR_CMC</b></dt>
</dl>
</td>
<td width="60%">
Full CMC

</td>
</tr>
<tr>
<td width="40%"><a id="XECR_PKCS10_V1_5"></a><a id="xecr_pkcs10_v1_5"></a><dl>
<dt><b>XECR_PKCS10_V1_5</b></dt>
</dl>
</td>
<td width="60%">
PKCS 10

</td>
</tr>
<tr>
<td width="40%"><a id="XECR_PKCS10_V2_0"></a><a id="xecr_pkcs10_v2_0"></a><dl>
<dt><b>XECR_PKCS10_V2_0</b></dt>
</dl>
</td>
<td width="60%">
PKCS 10 version 2

</td>
</tr>
<tr>
<td width="40%"><a id="XECR_PKCS7"></a><a id="xecr_pkcs7"></a><dl>
<dt><b>XECR_PKCS7</b></dt>
</dl>
</td>
<td width="60%">
PKCS 7

</td>
</tr>
</table>

### -param strDNName [in]

This parameter can be <b>NULL</b>; otherwise, this parameter specifies the distinguished name (DN) of the entity for which the request is being made. The DN name must follow the <a href="/windows/desktop/SecGloss/x-gly">X.500</a> naming convention, for example "CN=User, O=Microsoft". If a two-letter prefix does not exist, an OID may be provided instead.

### -param Usage [in]

An <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) that describes the purpose of the certificate being generated, for example, individual or commercial Authenticode certificate, or client authentication. You can also specify multiple OIDs separated by a comma.

### -param pstrRequest [out]

A pointer to a <b>BSTR</b> (BASE64_HEADER format) that receives the request. When you have finished using the <b>BSTR</b>, free it by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a <b>String</b> (BASE64_HEADER format) that contains the request.

## -remarks

When this method is called from script, the method displays a user interface that asks whether the user will allow creation of a  certificate request. If a .pvk or .spc file was specified, the method displays a user interface that asks whether the user will allow a write operation to the file system.


#### Examples


```cpp
BSTR bstrDN = NULL;
BSTR bstrReq = NULL;
ICEnroll4 * pEnroll4 = NULL;
HRESULT hr;

hr = CoInitializeEx( NULL, COINIT_APARTMENTTHREADED );
if (FAILED(hr))
{
    printf("Failed CoInitializeEx - %x\n", hr);
    goto error;
}

hr = CoCreateInstance( __uuidof(CEnroll),
                       NULL,
                       CLSCTX_INPROC_SERVER,
                       __uuidof(ICEnroll4),
                       (void **)&pEnroll4);
if (FAILED(hr))
{
    printf("Failed CoCreateInstance - pEnroll4 [%x]\n", hr);
    goto error;
}

// generate the DN for the cert request
bstrDN = SysAllocString( TEXT("CN=Your Name")   // common name
                         TEXT(",OU=Your Unit")  // org unit
                         TEXT(",O=Your Org")    // organization
                         TEXT(",L=Your City")   // locality
                         TEXT(",S=Your State")  // state
                         TEXT(",C=Your Country") );  // country/region

// create the CMC request
hr = pEnroll4->createRequest( XECR_CMC,
                              bstrDN,
                              NULL,
                              &bstrReq );
if (FAILED(hr))
{
        printf("Failed createRequest - pEnroll4 [%x]\n", hr);
        goto error;
}
else
    // do something with the CMC (bstrReq);

error:

//clean up resources, and so on
if ( bstrDN )
    SysFreeString( bstrDN );
if ( bstrReq )
    SysFreeString( bstrReq );
if ( pEnroll4 )
    pEnroll4->Release();

CoUninitialize();

```
