---
UID: NF:certif.ICertServerPolicy.EnumerateExtensions
title: ICertServerPolicy::EnumerateExtensions (certif.h)
description: Retrieves the object identifier (OID) of the current extension and moves the internal enumeration pointer to the next extension.
helpviewer_keywords: ["CCertServerPolicy object [Security]","EnumerateExtensions method","EnumerateExtensions","EnumerateExtensions method [Security]","EnumerateExtensions method [Security]","CCertServerPolicy object","EnumerateExtensions method [Security]","ICertServerPolicy interface","ICertServerPolicy interface [Security]","EnumerateExtensions method","ICertServerPolicy.EnumerateExtensions","ICertServerPolicy::EnumerateExtensions","_certsrv_icertserverpolicy_enumerateextensions","certif/ICertServerPolicy::EnumerateExtensions","security.icertserverpolicy_enumerateextensions"]
old-location: security\icertserverpolicy_enumerateextensions.htm
tech.root: security
ms.assetid: 565ff4d5-0d22-466d-8458-f98b992a1868
ms.date: 12/05/2018
ms.keywords: CCertServerPolicy object [Security],EnumerateExtensions method, EnumerateExtensions, EnumerateExtensions method [Security], EnumerateExtensions method [Security],CCertServerPolicy object, EnumerateExtensions method [Security],ICertServerPolicy interface, ICertServerPolicy interface [Security],EnumerateExtensions method, ICertServerPolicy.EnumerateExtensions, ICertServerPolicy::EnumerateExtensions, _certsrv_icertserverpolicy_enumerateextensions, certif/ICertServerPolicy::EnumerateExtensions, security.icertserverpolicy_enumerateextensions
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
 - ICertServerPolicy::EnumerateExtensions
 - certif/ICertServerPolicy::EnumerateExtensions
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
 - ICertServerPolicy.EnumerateExtensions
 - CCertServerPolicy.EnumerateExtensions
---

# ICertServerPolicy::EnumerateExtensions


## -description

The <b>EnumerateExtensions</b> method retrieves the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) of the current extension and moves the internal enumeration pointer to the next  extension.

## -parameters

### -param pstrExtensionName [out]

A pointer to a <b>BSTR</b> that contains the OID of the current extension.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK, and the <i>pstrExtensionName</i> parameter contains the OID  of the current extension. A value of S_FALSE is returned if the last extension was already enumerated.

To use this method, create a variable of <b>BSTR</b> type, set the variable equal to <b>NULL</b>, and pass the address of this variable as <i>pstrExtensionName</i>.

When you have finished using the <b>BSTR</b>, free it by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 Returns a string that contains the OID of the extension, or an empty string if the last extension was already enumerated.

## -remarks

This method enumerates certificate extensions recorded in the database, even those that are disabled and do not appear in the certificate. To determine whether an extension is disabled, use 
<a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-getcertificateextensionflags">GetCertificateExtensionFlags</a> to test the extension's EXTENSION_DISABLE_FLAG bit.

When done enumerating, call the <a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-enumerateextensionsclose">EnumerateExtensionsClose</a> method to free resources used by the enumeration calls.


#### Examples


``` syntax
#include <windows.h>
#include <stdio.h>
#include <Certif.h>

BSTR     bstrExt = NULL;
VARIANT  varExt;
LONG     ExtFlags;
HRESULT  hr;

VariantInit(&varExt);

// Enumerate the extensions.
while (S_OK ==
      (hr = pCertServerPol->EnumerateExtensions(&bstrExt)))
{
  // Retrieve the extension data.
  if (FAILED(pCertServerPol->GetCertificateExtension(
                             bstrExt,
                             PROPTYPE_BINARY,
                             &varExt)))
      printf("Failed GetCertificateExtension\n");
  else
  {
     // Retrieve the extension flags.
    if (FAILED(pCertServerPol->GetCertificateExtensionFlags(
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

<a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-enumerateextensionsclose">EnumerateExtensionsClose</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-enumerateextensionssetup">EnumerateExtensionsSetup</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-getcertificateextension">GetCertificateExtension</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-getcertificateextensionflags">GetCertificateExtensionFlags</a>



<a href="/windows/desktop/api/certif/nn-certif-icertserverpolicy">ICertServerPolicy</a>
