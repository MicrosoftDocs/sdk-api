---
UID: NF:certview.IEnumCERTVIEWEXTENSION.GetFlags
title: IEnumCERTVIEWEXTENSION::GetFlags (certview.h)
description: Retrieves the policy and origin flags of the current extension in the extension-enumeration sequence.
helpviewer_keywords: ["GetFlags","GetFlags method [Security]","GetFlags method [Security]","IEnumCERTVIEWEXTENSION interface","IEnumCERTVIEWEXTENSION interface [Security]","GetFlags method","IEnumCERTVIEWEXTENSION.GetFlags","IEnumCERTVIEWEXTENSION::GetFlags","_certsrv_ienumcertviewextension_getflags","certview/IEnumCERTVIEWEXTENSION::GetFlags","security.ienumcertviewextension_getflags"]
old-location: security\ienumcertviewextension_getflags.htm
tech.root: security
ms.assetid: c175eba9-ea7c-4018-876a-2db732cb57c4
ms.date: 12/05/2018
ms.keywords: GetFlags, GetFlags method [Security], GetFlags method [Security],IEnumCERTVIEWEXTENSION interface, IEnumCERTVIEWEXTENSION interface [Security],GetFlags method, IEnumCERTVIEWEXTENSION.GetFlags, IEnumCERTVIEWEXTENSION::GetFlags, _certsrv_ienumcertviewextension_getflags, certview/IEnumCERTVIEWEXTENSION::GetFlags, security.ienumcertviewextension_getflags
req.header: certview.h
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
 - IEnumCERTVIEWEXTENSION::GetFlags
 - certview/IEnumCERTVIEWEXTENSION::GetFlags
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
 - IEnumCERTVIEWEXTENSION.GetFlags
 - IEnumCERTVIEWEXTENSION.GetFlags
---

# IEnumCERTVIEWEXTENSION::GetFlags


## -description

The <b>GetFlags</b> method retrieves the policy and origin flags of the current extension in the extension-enumeration sequence.

 Both the policy and origin flags are returned in one variable, and bitmasks are provided to retrieve the individual values.

## -parameters

### -param pFlags [out]

A pointer to a <b>LONG</b> type that contains the policy and origin flags of the extension. This method fails if the <i>pFlags</i> parameter is set to <b>NULL</b>.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value represents the policy and origin values of the extension.

## -remarks

This method is used to retrieve the policy and origin flags of the extension currently referenced by the 
extension-enumeration sequence.

Policy flags provide information about the certificate extension and can be  set by the policy module.

Origin flags indicate the module that set the certificate extension and are set only by the server engine.

One or more policy flags can be returned from an extension. The following are predefined policy flags.

<table>
<tr>
<th>Policy flag value</th>
<th>Explanation</th>
</tr>
<tr>
<td>EXTENSION_CRITICAL_FLAG</td>
<td>This is a critical extension.</td>
</tr>
<tr>
<td>EXTENSION_DISABLE_FLAG</td>
<td>Extension will not be used.</td>
</tr>
</table>
 

One of the following origin flags can also be returned.

<table>
<tr>
<th>Origin flag value</th>
<th>Explanation</th>
</tr>
<tr>
<td>EXTENSION_ORIGIN_REQUEST</td>
<td>The extension was extracted from an array of extensions stored in the szOID_CERT_EXTENSIONS (1.3.6.1.4.1.311.2.1.14) or szOID_RSA_certExtensions (1.2.840.113549.1.9.14) attribute of a PKCS #10 request.</td>
</tr>
<tr>
<td>EXTENSION_ORIGIN_POLICY</td>
<td>The policy module set the extension.</td>
</tr>
<tr>
<td>EXTENSION_ORIGIN_ADMIN</td>
<td>The administrator set the extension.</td>
</tr>
<tr>
<td>EXTENSION_ORIGIN_SERVER</td>
<td>The server engine set the extension.</td>
</tr>
<tr>
<td>EXTENSION_ORIGIN_RENEWALCERT</td>
<td>The extension was extracted from the certificate stored in the szOID_RENEWAL_CERTIFICATE (1.3.6.1.4.1.311.13.1) attribute of a PKCS #10 renewal request.</td>
</tr>
<tr>
<td>EXTENSION_ORIGIN_IMPORTEDCERT</td>
<td>The extension was extracted from an imported certificate (the certificate was passed to 
<a href="/windows/desktop/api/certadm/nf-certadm-icertadmin-importcertificate">ICertAdmin::ImportCertificate</a>).</td>
</tr>
<tr>
<td>EXTENSION_ORIGIN_PKCS7</td>
<td>The extension was extracted from an array of extensions stored in the szOID_CERT_EXTENSIONS (1.3.6.1.4.1.311.2.1.14) or szOID_RSA_certExtensions (1.2.840.113549.1.9.14) attribute of a PKCS #7 request.</td>
</tr>
</table>
 

Predefined masks are provided for ease of use in determining which flags are set in the return value. The following masks are provided.

<table>
<tr>
<th>Mask value</th>
<th>Explanation</th>
</tr>
<tr>
<td>EXTENSION_POLICY_MASK</td>
<td>This value (0x0000FFFF) is used to examine policy flags.</td>
</tr>
<tr>
<td>EXTENSION_ORIGIN_MASK</td>
<td>This value (0x000F0000) is used to examine origin flags.</td>
</tr>
</table>
 

If the extension-enumeration sequence is not referencing a valid extension, <b>GetFlags</b> will fail. Use one of the following methods to navigate through the enumeration:

<ul>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-reset">IEnumCERTVIEWEXTENSION::Reset</a>: Moves to the next extension in the enumeration sequence.</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-next">IEnumCERTVIEWEXTENSION::Next</a>: Moves to the next extension in the enumeration sequence.</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-skip">IEnumCERTVIEWEXTENSION::Skip</a>: Skips a specified number of extensions.</li>
</ul>

#### Examples


```cpp
HRESULT  hr;
LONG     ExtFlags;

// pEnumExt is previously instantiated IEnumCERTVIEWEXTENSION object
hr = pEnumExt->GetFlags(&ExtFlags);
if (S_OK != hr)
    printf("Failed GetFlags - %x\n", hr);
else
{
    LONG ExtPol, ExtOrig;

    ExtPol = ExtFlags & EXTENSION_POLICY_MASK;
    if (ExtPol & EXTENSION_CRITICAL_FLAG)
        printf("The extension is critical\n");
    if (ExtPol & EXTENSION_DISABLE_FLAG )
        printf("The extension is disabled\n");

    ExtOrig = ExtFlags & EXTENSION_ORIGIN_MASK;
    switch (ExtOrig)
    {
        case EXTENSION_ORIGIN_REQUEST:
            printf("Extension originated by PKCS #10 Request\n");
            break;
        case EXTENSION_ORIGIN_POLICY:
            printf("Extension originated by Policy\n");
            break;
        case EXTENSION_ORIGIN_ADMIN:
            printf("Extension originated by Admin\n");
            break;
        case EXTENSION_ORIGIN_SERVER:
            printf("Extension originated by Server\n");
            break;
        case EXTENSION_ORIGIN_RENEWALCERT:
            printf("Extension originated by Renewal Request\n");
            break;
        case EXTENSION_ORIGIN_IMPORTEDCERT:
            printf("Extension originated by an imported "
                "certificate\n");
            break;
        case EXTENSION_ORIGIN_PKCS7:
            printf("Extension originated by PKCS #7 Request\n");
            break;
        default:
            printf("Unknown extension origin\n");
            break;
    }
}
```

## -see-also

<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewextension">IEnumCERTVIEWEXTENSION</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-getname">IEnumCERTVIEWEXTENSION::GetName</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-getvalue">IEnumCERTVIEWEXTENSION::GetValue</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-next">IEnumCERTVIEWEXTENSION::Next</a>