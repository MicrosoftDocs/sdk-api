---
UID: NF:certview.IEnumCERTVIEWEXTENSION.Clone
title: IEnumCERTVIEWEXTENSION::Clone (certview.h)
description: Creates a copy of the extension-enumeration sequence.
helpviewer_keywords: ["Clone","Clone method [Security]","Clone method [Security]","IEnumCERTVIEWEXTENSION interface","IEnumCERTVIEWEXTENSION interface [Security]","Clone method","IEnumCERTVIEWEXTENSION.Clone","IEnumCERTVIEWEXTENSION::Clone","_certsrv_ienumcertviewextension_clone","certview/IEnumCERTVIEWEXTENSION::Clone","security.ienumcertviewextension_clone"]
old-location: security\ienumcertviewextension_clone.htm
tech.root: security
ms.assetid: 2b8e19e4-459f-45f0-abb6-e1e0e115e0f5
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Security], Clone method [Security],IEnumCERTVIEWEXTENSION interface, IEnumCERTVIEWEXTENSION interface [Security],Clone method, IEnumCERTVIEWEXTENSION.Clone, IEnumCERTVIEWEXTENSION::Clone, _certsrv_ienumcertviewextension_clone, certview/IEnumCERTVIEWEXTENSION::Clone, security.ienumcertviewextension_clone
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
 - IEnumCERTVIEWEXTENSION::Clone
 - certview/IEnumCERTVIEWEXTENSION::Clone
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
 - IEnumCERTVIEWEXTENSION.Clone
 - IEnumCERTVIEWEXTENSION.Clone
---

# IEnumCERTVIEWEXTENSION::Clone


## -description

The <a href="/windows/desktop/api/certview/nn-certview-ienumcertviewextension">Clone</a> method creates a copy of the extension-enumeration sequence.

## -parameters

### -param ppenum [out]

A pointer to a pointer of <a href="/windows/desktop/api/certview/nn-certview-ienumcertviewextension">IEnumCERTVIEWEXTENSION</a> type. This method will fail if the <i>ppenum</i> parameter is <b>NULL</b>.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a cloned extension-enumeration sequence object.

## -remarks

The extension-enumeration sequence object is obtained by a call to the <a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-enumcertviewextension">IEnumCERTVIEWROW::EnumCertViewExtension</a> method.


#### Examples


```cpp
IEnumCERTVIEWEXTENSION * pEnumExt2 = NULL;
HRESULT                  hr;

// pEnumExt is previously instantiated IEnumCERTVIEWEXTENSION object
hr = pEnumExt->Clone(&pEnumExt2);
if (S_OK != hr)
    printf("Unable to clone IEnumCERTVIEWEXTENSION\n");
else
{
    // use cloned object as needed
    //...
}
// done using cloned object, free memory
if (NULL != pEnumExt2)
    pEnumExt2->Release();
```

## -see-also

<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewextension">IEnumCERTVIEWEXTENSION</a>