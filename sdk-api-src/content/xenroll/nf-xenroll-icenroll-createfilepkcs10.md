---
UID: NF:xenroll.ICEnroll.createFilePKCS10
title: ICEnroll::createFilePKCS10 (xenroll.h)
description: Creates a base64-encoded PKCS (ICEnroll.createFilePKCS10)
helpviewer_keywords: ["CEnroll object [Security]","createFilePKCS10 method","ICEnroll interface [Security]","createFilePKCS10 method","ICEnroll.createFilePKCS10","ICEnroll2 interface [Security]","createFilePKCS10 method","ICEnroll2::createFilePKCS10","ICEnroll3 interface [Security]","createFilePKCS10 method","ICEnroll3::createFilePKCS10","ICEnroll4 interface [Security]","createFilePKCS10 method","ICEnroll4::createFilePKCS10","ICEnroll::createFilePKCS10","createFilePKCS10","createFilePKCS10 method [Security]","createFilePKCS10 method [Security]","CEnroll object","createFilePKCS10 method [Security]","ICEnroll interface","createFilePKCS10 method [Security]","ICEnroll2 interface","createFilePKCS10 method [Security]","ICEnroll3 interface","createFilePKCS10 method [Security]","ICEnroll4 interface","security.icenroll4_createfilepkcs10","xenroll/ICEnroll2::createFilePKCS10","xenroll/ICEnroll3::createFilePKCS10","xenroll/ICEnroll4::createFilePKCS10","xenroll/ICEnroll::createFilePKCS10"]
old-location: security\icenroll4_createfilepkcs10.htm
tech.root: security
ms.assetid: 074c7321-6117-4261-836a-a2055c9e029d
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],createFilePKCS10 method, ICEnroll interface [Security],createFilePKCS10 method, ICEnroll.createFilePKCS10, ICEnroll2 interface [Security],createFilePKCS10 method, ICEnroll2::createFilePKCS10, ICEnroll3 interface [Security],createFilePKCS10 method, ICEnroll3::createFilePKCS10, ICEnroll4 interface [Security],createFilePKCS10 method, ICEnroll4::createFilePKCS10, ICEnroll::createFilePKCS10, createFilePKCS10, createFilePKCS10 method [Security], createFilePKCS10 method [Security],CEnroll object, createFilePKCS10 method [Security],ICEnroll interface, createFilePKCS10 method [Security],ICEnroll2 interface, createFilePKCS10 method [Security],ICEnroll3 interface, createFilePKCS10 method [Security],ICEnroll4 interface, security.icenroll4_createfilepkcs10, xenroll/ICEnroll2::createFilePKCS10, xenroll/ICEnroll3::createFilePKCS10, xenroll/ICEnroll4::createFilePKCS10, xenroll/ICEnroll::createFilePKCS10
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
 - ICEnroll::createFilePKCS10
 - xenroll/ICEnroll::createFilePKCS10
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
 - ICEnroll4.createFilePKCS10
 - ICEnroll3.createFilePKCS10
 - ICEnroll2.createFilePKCS10
 - ICEnroll.createFilePKCS10
 - CEnroll.createFilePKCS10
---

# ICEnroll::createFilePKCS10


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>createFilePKCS10</b> method creates a base64-encoded PKCS #10 <a href="/windows/desktop/SecGloss/c-gly">certificate request</a> and saves it in a file. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a> interface.

This method differs from 
the <a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-createpkcs10">createPKCS10</a> method only in saving the base64-encoded PKCS #10 <a href="/windows/desktop/SecGloss/c-gly">certificate request</a> (in <b>BSTR</b> form) to the file specified by the <i>wszPKCS10FileName</i> parameter.

## -parameters

### -param DNName [in]

The distinguished name (DN) of the entity for which the request is being made. <i>DNName</i> must follow the <a href="/windows/desktop/SecGloss/x-gly">X.500</a> naming convention. For example "CN=User, O=Microsoft". If a two-letter prefix does not exist, an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) may be provided instead.

### -param Usage [in]

An <a href="/windows/desktop/SecGloss/o-gly">OID</a> that describes the purpose of the certificate being generated, for example, individual or commercial Authenticode certificate, or client authentication. You can also specify multiple OIDs separated by a comma.

The OID is passed through to the PKCS #10 request. The control does not examine the OID.

### -param wszPKCS10FileName [in]

The name of the file in which the base64-encoded PKCS #10 (in <b>BSTR</b> form) is saved. The contents of this file may be submitted to a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> for processing.

## -returns

<h3>VB</h3>
The return value is an <b>HRESULT</b>. A value of <b>S_OK</b> indicates success.

If the method fails, the return value is an <b>HRESULT</b> indicating the error. For a list of common error codes, see 
<a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

By default, the Microsoft Base Cryptographic Provider is used, and a unique signature key is created.

When this method is called from script, the method displays a user interface that asks whether the user will allow creation of a  certificate request and whether the user will allow a write operation to the file system.


#### Examples


```cpp
BSTR bstrDN = NULL;
BSTR bstrOID = NULL;
BSTR bstrFileName = NULL;
ICEnroll4 * pEnroll = NULL;
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
                       (void **)&pEnroll);
if (FAILED(hr))
{
    printf("Failed CoCreateInstance - pEnroll [%x]\n", hr);
    goto error;
}

// Generate the DN for the cert request.
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

// Generate the OID. For example, "1.3.6.1.4.1.311.2.1.21"
bstrOID = SysAllocString(TEXT("<OIDHERE>"));
if (NULL == bstrOID)
{
    printf("Memory allocation failed for bstrOID.\n");
    goto error;
}

// Specify the file name, for example, "myPKCS10.req"
bstrFileName = SysAllocString(TEXT("<FILENAMEHERE>"));
if (NULL == bstrFileName)
{
    printf("Memory allocation failed for bstrFileName.\n");
    goto error;
}

// Create the PKCS10 (stored in a file).
hr = pEnroll->createFilePKCS10( bstrDN, bstrOID, bstrFileName );
if (FAILED(hr))
{
   printf("Failed createFilePKCS10 - %x\n", hr);
   goto error;
}
else
    printf("Successfully created file containing PKCS10\n");

error:
// Clean up resources and so on.

if ( bstrFileName )
    SysFreeString( bstrFileName );

if ( bstrDN )
    SysFreeString( bstrDN );

if ( bstrOID )
    SysFreeString( bstrOID );

if ( pEnroll )
       pEnroll->Release();

CoUninitialize();

```
