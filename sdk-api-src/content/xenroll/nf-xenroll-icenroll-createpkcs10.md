---
UID: NF:xenroll.ICEnroll.createPKCS10
title: ICEnroll::createPKCS10 (xenroll.h)
description: Creates a base64-encoded PKCS (ICEnroll.createPKCS10)
helpviewer_keywords: ["CEnroll object [Security]","createPKCS10 method","ICEnroll interface [Security]","createPKCS10 method","ICEnroll.createPKCS10","ICEnroll2 interface [Security]","createPKCS10 method","ICEnroll2::createPKCS10","ICEnroll3 interface [Security]","createPKCS10 method","ICEnroll3::createPKCS10","ICEnroll4 interface [Security]","createPKCS10 method","ICEnroll4::createPKCS10","ICEnroll::createPKCS10","createPKCS10","createPKCS10 method [Security]","createPKCS10 method [Security]","CEnroll object","createPKCS10 method [Security]","ICEnroll interface","createPKCS10 method [Security]","ICEnroll2 interface","createPKCS10 method [Security]","ICEnroll3 interface","createPKCS10 method [Security]","ICEnroll4 interface","security.icenroll4_createpkcs10","xenroll/ICEnroll2::createPKCS10","xenroll/ICEnroll3::createPKCS10","xenroll/ICEnroll4::createPKCS10","xenroll/ICEnroll::createPKCS10"]
old-location: security\icenroll4_createpkcs10.htm
tech.root: security
ms.assetid: b8e841c1-f16e-4f3a-94f2-ef6708c88910
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],createPKCS10 method, ICEnroll interface [Security],createPKCS10 method, ICEnroll.createPKCS10, ICEnroll2 interface [Security],createPKCS10 method, ICEnroll2::createPKCS10, ICEnroll3 interface [Security],createPKCS10 method, ICEnroll3::createPKCS10, ICEnroll4 interface [Security],createPKCS10 method, ICEnroll4::createPKCS10, ICEnroll::createPKCS10, createPKCS10, createPKCS10 method [Security], createPKCS10 method [Security],CEnroll object, createPKCS10 method [Security],ICEnroll interface, createPKCS10 method [Security],ICEnroll2 interface, createPKCS10 method [Security],ICEnroll3 interface, createPKCS10 method [Security],ICEnroll4 interface, security.icenroll4_createpkcs10, xenroll/ICEnroll2::createPKCS10, xenroll/ICEnroll3::createPKCS10, xenroll/ICEnroll4::createPKCS10, xenroll/ICEnroll::createPKCS10
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
 - ICEnroll::createPKCS10
 - xenroll/ICEnroll::createPKCS10
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
 - ICEnroll4.createPKCS10
 - ICEnroll3.createPKCS10
 - ICEnroll2.createPKCS10
 - ICEnroll.createPKCS10
 - CEnroll.createPKCS10
---

# ICEnroll::createPKCS10


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>createPKCS10</b> method creates a base64-encoded PKCS #10 <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a> interface.

 This base64-encoded PKCS #10 certificate request (in <b>BSTR</b> form) can be submitted to a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> to request  that a certificate be issued to the person or entity whose information it contains.

## -parameters

### -param DNName [in]

The distinguished name (DN) of the entity for which the request is being made. In this parameter, the DN name must follow the <a href="/windows/desktop/SecGloss/x-gly">X.500</a> naming convention. For example "CN=User, O=Microsoft". If a two-letter prefix does not exist, an <a href="/windows/desktop/SecGloss/o-gly">OID</a> may be provided instead.

### -param Usage [in]

An <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) that describes the purpose of the certificate being generated. For example, Individual or Commercial Authenticode certificate, or Client Authentication. You can also specify multiple OIDs separated by a comma.

The  OID is passed through to the PKCS #10 request. For general extensibility and ease of understanding, the control does not attempt to understand specific-purpose OIDs. Therefore if you specify a Client Authentication OID, the generated key will still be a signature key, not an <a href="/windows/desktop/SecGloss/e-gly">exchange key</a>.

### -param pPKCS10 [in]

The returned base64-encoded PKCS10 certificate request.

## -returns

<h3>C++</h3>
The return value is an <b>HRESULT</b>. A value of <b>S_OK</b> indicates success. Upon successful completion of this function, <i>pPKCS10</i> will contain a base64-encoded PKCS #10 request (in <b>BSTR</b> form). The format is such that it can be directly posted to a web server for processing.

<h3>VB</h3>
The returned base64-encoded PKCS10 certificate request.

## -remarks

By default, the Microsoft Base Cryptographic Provider is used, PROV_RSA_FULL is the provider type, a signature key is created, and a unique new key set is created.

When this method is called from script, the method displays a user interface that asks whether the user will allow creation of a  certificate request.


#### Examples


```cpp
BSTR bstrDN = NULL;
BSTR bstrReq = NULL;
BSTR bstrOID = NULL;
ICEnroll4 * pEnroll = NULL;
HRESULT hr;

// initialize COM
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
                       (void **)&pEnroll);
if (FAILED(hr))
{
    printf("Failed CoCreateInstance - pEnroll [%x]\n", hr);
    goto error;
}
// generate the DN for the cert request
bstrDN = SysAllocString( TEXT("CN=Your Name")   // common name
                         TEXT(",OU=Your Unit")  // org unit
                         TEXT(",O=Your Org")    // organization
                         TEXT(",L=Your City")   // locality
                         TEXT(",S=Your State")  // state
                         TEXT(",C=Your Country") );  // country/region
if (NULL == bstrDN)
{
    printf("Memory allocation failed for bstrDN.\n");
    goto error;
}

// generate the OID, for example, "1.3.6.1.4.1.311.2.1.21".
bstrOID = SysAllocString(TEXT("<OIDHERE>"));
if (NULL == bstrOID)
{
    printf("Memory allocation failed for bstrOID.\n");
    goto error;
}

// create the PKCS10
hr = pEnroll->createPKCS10( bstrDN, bstrOID, &bstrReq );
if (FAILED(hr))
{
    printf("Failed createPKCS10 - %x\n", hr);
    goto error;
}
else
    // do something with the PKCS10 (bstrReq);

error:

//clean up resources, and so on
if ( bstrDN )
    SysFreeString( bstrDN );
if ( bstrOID )
    SysFreeString( bstrOID );
if ( bstrReq )
    SysFreeString( bstrReq );
if ( pEnroll )
    pEnroll->Release();

CoUninitialize();

```
