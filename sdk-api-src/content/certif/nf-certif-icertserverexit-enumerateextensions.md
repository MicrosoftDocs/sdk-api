---
UID: NF:certif.ICertServerExit.EnumerateExtensions
title: ICertServerExit::EnumerateExtensions (certif.h)
description: Returns the object identifier (OID) string (also known as the extension name) of the next certificate extension to be enumerated, then increments the internal pointer to the following extension.
helpviewer_keywords: ["CCertServerExit object [Security]","EnumerateExtensions method","EnumerateExtensions","EnumerateExtensions method [Security]","EnumerateExtensions method [Security]","CCertServerExit object","EnumerateExtensions method [Security]","ICertServerExit interface","ICertServerExit interface [Security]","EnumerateExtensions method","ICertServerExit.EnumerateExtensions","ICertServerExit::EnumerateExtensions","_certsrv_icertserverexit_enumerateextensions","certif/ICertServerExit::EnumerateExtensions","security.icertserverexit_enumerateextensions"]
old-location: security\icertserverexit_enumerateextensions.htm
tech.root: security
ms.assetid: 8726f5fa-dc85-4357-b73a-013842d6ab78
ms.date: 12/05/2018
ms.keywords: CCertServerExit object [Security],EnumerateExtensions method, EnumerateExtensions, EnumerateExtensions method [Security], EnumerateExtensions method [Security],CCertServerExit object, EnumerateExtensions method [Security],ICertServerExit interface, ICertServerExit interface [Security],EnumerateExtensions method, ICertServerExit.EnumerateExtensions, ICertServerExit::EnumerateExtensions, _certsrv_icertserverexit_enumerateextensions, certif/ICertServerExit::EnumerateExtensions, security.icertserverexit_enumerateextensions
req.header: certif.h
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
req.dll: Certcli.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertServerExit::EnumerateExtensions
 - certif/ICertServerExit::EnumerateExtensions
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
 - ICertServerExit.EnumerateExtensions
 - CCertServerExit.EnumerateExtensions
---

# ICertServerExit::EnumerateExtensions


## -description

The <b>EnumerateExtensions</b> method returns the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) string (also known as the extension name) of the next certificate extension to be enumerated, then increments the internal pointer to the following extension.

 Before calling <b>EnumerateExtensions</b>, an application calls 
<a href="/windows/desktop/api/certif/nf-certif-icertserverexit-enumerateextensionssetup">ICertServerExit::EnumerateExtensionsSetup</a>. When done enumerating, an application calls 
<a href="/windows/desktop/api/certif/nf-certif-icertserverexit-enumerateextensionsclose">ICertServerExit::EnumerateExtensionsClose</a>.

## -parameters

### -param pstrExtensionName [out]

A pointer to the enumerated extension name.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK, and *<i>pstrExtensionName</i> is set to the <b>BSTR</b> that contains the name of the enumerated extension. A value of S_FALSE is returned if the last extension was already enumerated.

To use this method, create a variable of <b>BSTR</b> type, set the variable equal to <b>NULL</b>, and pass the address of this variable as <i>pstrExtensionName</i>.

When you have finished using the <b>BSTR</b>, free it by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 Returns a string that contains the name of the enumerated extension, or an empty string if the last extension was already enumerated.

## -remarks

This method enumerates certificate extensions recorded in the database, even those that are disabled and do not appear in the certificate. To determine whether an extension is disabled, use 
<a href="/windows/desktop/api/certif/nf-certif-icertserverexit-getcertificateextensionflags">ICertServerExit::GetCertificateExtensionFlags</a> to test the extension's EXTENSION_DISABLE_FLAG bit.


#### Examples


```cpp
BSTR     bstrExt = NULL;
VARIANT  varExt;
LONG     ExtFlags;
HRESULT  hr;

VariantInit(&varExt);

// Enumerate the extensions.
while (S_OK ==
      (hr = pCertServerExit->EnumerateExtensions(&bstrExt)))
{
  // Retrieve the extension data.
  if (FAILED(pCertServerExit->GetCertificateExtension(
                              bstrExt,
                              PROPTYPE_BINARY,
                              &varExt)))
      printf("Failed GetCertificateExtension\n");
  else
  {
     // Retrieve the extension flags.
    if (FAILED(pCertServerExit->GetCertificateExtensionFlags(
                                &ExtFlags)))
        printf("Failed GetCertificateExtensionFlags\n");
    else
        // This sample will display the extension OID string,
        // the extension flags (in hex) and
        // the length of the BSTR binary ASN-encode extension.
        printf("Extension: %ws\tFlags:%x\tLength:%u\n",
               bstrExt,
               ExtFlags,
               SysStringByteLen(varExt.bstrVal));
  }
}
// Determine if hr was S_FALSE, meaning the enumeration 
// was completed, or some other error.
if (S_FALSE != hr)
    printf("Failed EnumerateExtensions - %x\n", hr);
// Free BSTR resource.
if (NULL != bstrExt)
    SysFreeString(bstrExt);
// Free VARIANT resource.
    VariantClear(&varExt);
```

## -see-also

<a href="/windows/desktop/api/certif/nn-certif-icertserverexit">ICertServerExit</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverexit-enumerateextensionsclose">ICertServerExit::EnumerateExtensionsClose</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverexit-enumerateextensionssetup">ICertServerExit::EnumerateExtensionsSetup</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverexit-getcertificateextension">ICertServerExit::GetCertificateExtension</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverexit-getcertificateextensionflags">ICertServerExit::GetCertificateExtensionFlags</a>