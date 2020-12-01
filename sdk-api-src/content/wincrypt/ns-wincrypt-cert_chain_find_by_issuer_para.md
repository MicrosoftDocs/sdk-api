---
UID: NS:wincrypt._CERT_CHAIN_FIND_BY_ISSUER_PARA
title: CERT_CHAIN_FIND_BY_ISSUER_PARA (wincrypt.h)
description: Contains information used in the CertFindChainInStore function to build certificate chains.
helpviewer_keywords: ["*PCERT_CHAIN_FIND_BY_ISSUER_PARA","*PCERT_CHAIN_FIND_ISSUER_PARA","AT_KEYEXCHANGE","AT_SIGNATURE","CERT_CHAIN_FIND_BY_ISSUER_PARA","CERT_CHAIN_FIND_BY_ISSUER_PARA structure [Security]","CERT_CHAIN_FIND_ISSUER_PARA","_CERT_CHAIN_FIND_BY_ISSUER_PARA","_CERT_CHAIN_FIND_BY_ISSUER_PARA structure [Security]","_crypto2_cert_chain_find_by_issuer_para","security.cert_chain_find_by_issuer_para","wincrypt/CERT_CHAIN_FIND_BY_ISSUER_PARA"]
old-location: security\cert_chain_find_by_issuer_para.htm
tech.root: security
ms.assetid: 7dee640e-6bad-4d3c-910f-da928a8682c9
ms.date: 12/05/2018
ms.keywords: '*PCERT_CHAIN_FIND_BY_ISSUER_PARA, *PCERT_CHAIN_FIND_ISSUER_PARA, AT_KEYEXCHANGE, AT_SIGNATURE, CERT_CHAIN_FIND_BY_ISSUER_PARA, CERT_CHAIN_FIND_BY_ISSUER_PARA structure [Security], CERT_CHAIN_FIND_ISSUER_PARA, _CERT_CHAIN_FIND_BY_ISSUER_PARA, _CERT_CHAIN_FIND_BY_ISSUER_PARA structure [Security], _crypto2_cert_chain_find_by_issuer_para, security.cert_chain_find_by_issuer_para, wincrypt/CERT_CHAIN_FIND_BY_ISSUER_PARA'
req.header: wincrypt.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CERT_CHAIN_FIND_ISSUER_PARA, *PCERT_CHAIN_FIND_ISSUER_PARA, CERT_CHAIN_FIND_BY_ISSUER_PARA, *PCERT_CHAIN_FIND_BY_ISSUER_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_CHAIN_FIND_BY_ISSUER_PARA
 - wincrypt/_CERT_CHAIN_FIND_BY_ISSUER_PARA
 - PCERT_CHAIN_FIND_ISSUER_PARA
 - wincrypt/PCERT_CHAIN_FIND_ISSUER_PARA
 - CERT_CHAIN_FIND_BY_ISSUER_PARA
 - wincrypt/CERT_CHAIN_FIND_BY_ISSUER_PARA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - _CERT_CHAIN_FIND_BY_ISSUER_PARA
---

# CERT_CHAIN_FIND_BY_ISSUER_PARA structure


## -description

The <b>CERT_CHAIN_FIND_BY_ISSUER_PARA</b> structure contains information used in the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindchaininstore">CertFindChainInStore</a> function to build certificate chains.

## -struct-fields

### -field cbSize

Contains the size of this structure, in bytes. This size should not be hard-coded. It should be set at compile time by using the <b>sizeof</b> operator as shown in the following example.


```cpp
CERT_CHAIN_FIND_BY_ISSUER_PARA findParams;
findParams.cbSize = sizeof(CERT_CHAIN_FIND_BY_ISSUER_PARA);
```

### -field pszUsageIdentifier

A pointer to a null-terminated ANSI string that contains the usage identifier to be matched. If this member is <b>NULL</b>, a certificate with any usage can be a match.

### -field dwKeySpec

Contains the key specification value to be matched. This can be one of the following values. If this parameter is zero, any certificate can match.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AT_KEYEXCHANGE"></a><a id="at_keyexchange"></a><dl>
<dt><b>AT_KEYEXCHANGE</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
The key can be used to encrypt or sign depending on the algorithm.

</td>
</tr>
<tr>
<td width="40%"><a id="AT_SIGNATURE"></a><a id="at_signature"></a><dl>
<dt><b>AT_SIGNATURE</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
The key can be used for signing.

</td>
</tr>
</table>

### -field dwAcquirePrivateKeyFlags

When the <i>dwFindFlags</i> parameter of the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindchaininstore">CertFindChainInStore</a> function contains <b>CERT_CHAIN_FIND_BY_ISSUER_COMPARE_KEY_FLAG</b>, the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecertificateprivatekey">CryptAcquireCertificatePrivateKey</a> function is called to do the public key comparison. In this case, this member is passed as the <i>dwFlags</i> parameter of the <b>CryptAcquireCertificatePrivateKey</b> function. For possible values for this member and their meanings, see the <i>dwFlags</i> parameter of the <b>CryptAcquireCertificatePrivateKey</b> function.

### -field cIssuer

Contains the number of elements in the <b>rgIssuer</b> array. If this member is zero, any issuer can be a match.

### -field rgIssuer

An array of <a href="/windows/desktop/SecGloss/x-gly">X.509</a>, <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoded issuer name <a href="/windows/desktop/SecGloss/b-gly">BLOBs</a> to match. If this member is <b>NULL</b> or the callback function returns <b>TRUE</b>, a new element is added to the chain for the certificate having a <a href="/windows/desktop/SecGloss/p-gly">private key</a> with the specified KeySpec and <a href="/windows/desktop/SecGloss/e-gly">enhanced key usage</a>.

### -field pfnFindCallback

A pointer to a <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_chain_find_by_issuer_callback">CertChainFindByIssuerCallback</a> callback function that allows the application to filter the certificates that chains are created for. If this member is <b>NULL</b>, a chain is built for every certificate found. If this member is not <b>NULL</b>, a chain will be built for the certificate found based on the return value of the callback function.

### -field pvFindArg

An application-defined value that will be passed as the <i>pvFindArg</i> parameter of the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_chain_find_by_issuer_callback">CertChainFindByIssuerCallback</a> callback function pointed to by the <b>pfnFindCallback</b> member of this structure.

### -field pdwIssuerChainIndex

A pointer to a <b>DWORD</b> value that receives the zero-based index of the chain that matches the issuer. If this member is <b>NULL</b>, it is not used.

If <b>cIssuer</b> is zero, this member is not used.

This member is only defined if the <b>CERT_CHAIN_FIND_BY_ISSUER_PARA_HAS_EXTRA_FIELDS</b> macro is defined.

### -field pdwIssuerElementIndex

A pointer to a <b>DWORD</b> value that receives the zero-based index of the element in the chain of the certificate of the issuer. If this member is <b>NULL</b>, it is not used.

If <b>cIssuer</b> is zero, this member is not used.

This  member is set to the index of the found certificate plus one to provide the index of  the certificate of the issuer. Because of this, a partial chain or a self-signed certificate that matches the name BLOB may cause <b>pdwIssuerElementIndex</b> to point past the last certificate in the chain. This situation can be detected by comparing the contents of <b>pdwIssuerElementIndex</b> with the <b>cElement</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_simple_chain">CERT_SIMPLE_CHAIN</a> structure to make sure the index is valid.

This member is only defined if the <b>CERT_CHAIN_FIND_BY_ISSUER_PARA_HAS_EXTRA_FIELDS</b> macro is defined.

## -remarks

The <b>pdwIssuerChainIndex</b> and <b>pdwIssuerElementIndex</b> members are only available if the <b>CERT_CHAIN_FIND_BY_ISSUER_PARA_HAS_EXTRA_FIELDS</b> macro is defined. If the <b>CERT_CHAIN_FIND_BY_ISSUER_PARA_HAS_EXTRA_FIELDS</b> macro is defined, the application must initialize all unused fields to zero.


#### Examples

The following pseudocode shows how to use the <b>pdwIssuerChainIndex</b> and <b>pdwIssuerElementIndex</b> members of this structure to access the certificate of the issuer.


```cpp
CERT_CHAIN_FIND_BY_ISSUER_PARA findParams;
PCCERT_CHAIN_CONTEXT pChainContext = NULL;
DWORD dwChainIndex = 0;
DWORD dwElementIndex = 0;
findParams.pdwIssuerChainIndex = &dwChainIndex;
findParams.pdwIssuerElementIndex = &dwElementIndex;

pChainContext = CertFindChainInStore(
    hCertStore,
    X509_ASN_ENCODING,
    0,
    CERT_CHAIN_FIND_BY_ISSUER,
    (LPVOID)&findParams,
    NULL);
if(pChainContext)
{
    // Make sure the element index is valid.
    if(dwElementIndex < pChainContext->
        rgpChain[dwChainIndex]->cElement)
    {
        PCERT_CHAIN_ELEMENT pIssuerElement;
        pIssuerElement = pChainContext->
            rgpChain[dwChainIndex]->rgpElement[dwElementIndex];
       // ...
    }

    // Free the certificate chain.
    CertFreeCertificateChain(pChainContext);
}
```

## -see-also

<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_chain_find_by_issuer_callback">CertChainFindByIssuerCallback</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindchaininstore">CertFindChainInStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecertificateprivatekey">CryptAcquireCertificatePrivateKey</a>