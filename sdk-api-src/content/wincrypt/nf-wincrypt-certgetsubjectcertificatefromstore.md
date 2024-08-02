---
UID: NF:wincrypt.CertGetSubjectCertificateFromStore
title: CertGetSubjectCertificateFromStore function (wincrypt.h)
description: Returns from a certificate store a subject certificate context uniquely identified by its issuer and serial number.
helpviewer_keywords: ["CertGetSubjectCertificateFromStore","CertGetSubjectCertificateFromStore function [Security]","_crypto2_certgetsubjectcertificatefromstore","security.certgetsubjectcertificatefromstore","wincrypt/CertGetSubjectCertificateFromStore"]
old-location: security\certgetsubjectcertificatefromstore.htm
tech.root: security
ms.assetid: 61d73501-91b1-4498-b1a3-17392360c700
ms.date: 12/05/2018
ms.keywords: CertGetSubjectCertificateFromStore, CertGetSubjectCertificateFromStore function [Security], _crypto2_certgetsubjectcertificatefromstore, security.certgetsubjectcertificatefromstore, wincrypt/CertGetSubjectCertificateFromStore
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertGetSubjectCertificateFromStore
 - wincrypt/CertGetSubjectCertificateFromStore
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertGetSubjectCertificateFromStore
---

# CertGetSubjectCertificateFromStore function


## -description

The <b>CertGetSubjectCertificateFromStore</b> function returns from a <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> a subject certificate context uniquely identified by its issuer and serial number.

## -parameters

### -param hCertStore [in]

A handle of a <a href="/windows/desktop/SecGloss/c-gly">certificate store</a>.

### -param dwCertEncodingType [in]

The type of encoding used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pCertId [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a> structure. Only the <b>Issuer</b> and <b>SerialNumber</b> members are used.

## -returns

If the function succeeds, the function returns a pointer to a read-only 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>. The <b>CERT_CONTEXT</b> must be freed by calling 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a>.

The returned certificate might not be valid. Usually, it is verified when getting its issuer certificate (<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetissuercertificatefromstore">CertGetIssuerCertificateFromStore</a>).

For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. One possible error code is the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The subject certificate was not found in the store.

</td>
</tr>
</table>

## -remarks

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext">CertDuplicateCertificateContext</a> can be called to make a duplicate certificate.


#### Examples

The following example shows retrieving a subject's certificate context, uniquely identified by its issuer and serial number, from the certificate store. For an example that includes the complete context for this example, see 
<a href="/windows/desktop/SecCrypto/example-c-program-signing-encoding-decoding-and-verifying-a-message">Example C Program: Signing, Encoding, Decoding, and Verifying a Message</a>.


``` syntax

#include <windows.h>
#include <stdio.h>
#include <Wincrypt.h>

#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)

void main()
{
//-------------------------------------------------------------------
// Declare and initialize variables.

HCERTSTORE hStoreHandle;           // certificate store handle
HCRYPTMSG hMsg;
PCCERT_CONTEXT pSignerCertContext;
DWORD          cbSignerCertInfo;
PCERT_INFO     pSignerCertInfo;
//-------------------------------------------------------------------
//  This code is based on hMsg being a signed, encoded message
//  read from a file or otherwise acquired. For detailed code, see 
//  "Example C Program: Signing, Encoding, Decoding, and Verifying a 
//  Message."

//-------------------------------------------------------------------
// Retrieve the signer CERT_INFO from the message by first getting
// the size of the memory required for the certificate.

if(CryptMsgGetParam(
   hMsg,                         // handle to the message
   CMSG_SIGNER_CERT_INFO_PARAM,  // parameter type
   0,                            // index
   NULL,   
   &cbSignerCertInfo))           // size of the returned information

{
   printf("%d bytes needed for the buffer.\n", cbSignerCertInfo);
}
else
{
   printf("Verify SIGNER_CERT_INFO #1 failed\n");
   exit(1);
}

//-------------------------------------------------------------------
// Allocate memory.

pSignerCertInfo = (PCERT_INFO) malloc(cbSignerCertInfo);
if (!pSignerCertInfo)
{
    printf("Verify memory allocation failed.\n");
    exit(1);
}

//-------------------------------------------------------------------
// Get the message certificate information (CERT_INFO
// structure).

if(!(CryptMsgGetParam(
     hMsg,                         // handle to the message
     CMSG_SIGNER_CERT_INFO_PARAM,  // parameter type
     0,                            // index
     pSignerCertInfo,              // address for returned information
     &cbSignerCertInfo)))          // size of the returned information

{
    printf("Verify SIGNER_CERT_INFO #2 failed.\n");
    exit(1);
}

//-------------------------------------------------------------------
// Open a certificate store in memory using CERT_STORE_PROV_MSG,
// which initializes it with the certificates from the message.

hStoreHandle = CertOpenStore(
   CERT_STORE_PROV_MSG,         // store provider type 
   MY_ENCODING_TYPE,            // encoding type
   NULL,                        // cryptographic provider
                                // use NULL for the default
   0,                           // flags
   hMsg));                      // handle to the message
   
if (hStoreHandle)
{
    printf("The certificate store to be used for message\n ");
    printf("    verification has been opened. \n");
}
else  
{
    printf("Verify open store failed.\n");
    exit(1);
}

//-------------------------------------------------------------------
// Find the signer's certificate in the store.

pSignerCertContext = CertGetSubjectCertificateFromStore(
    hStoreHandle,       // handle to store
    MY_ENCODING_TYPE,   // encoding type
    pSignerCertInfo));  // pointer to retrieved CERT_CONTEXT
    
if(pSignerCertContext)
{

//-------------------------------------------------------------------
// Use the certificate retrieved from the message. For some 
// processing that can be done with the certificate, see the full
// program.

}
//-------------------------------------------------------------------
// Clean up.

if(pSignerCertInfo)
   free(pSignerCertInfo);
if(pSignerCertContext)
   CertFreeCertificateContext(pSignerCertContext); 
if(hStoreHandle)
   CertCloseStore(hStoreHandle, CERT_CLOSE_STORE_FORCE_FLAG);
if(hMsg)
   CryptMsgClose(hMsg);

}
```


## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext">CertDuplicateCertificateContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetissuercertificatefromstore">CertGetIssuerCertificateFromStore</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Functions</a>
