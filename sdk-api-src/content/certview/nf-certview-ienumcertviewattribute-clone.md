---
UID: NF:certview.IEnumCERTVIEWATTRIBUTE.Clone
title: IEnumCERTVIEWATTRIBUTE::Clone (certview.h)
description: Creates a copy of the attribute-enumeration sequence object in its current state.
helpviewer_keywords: ["Clone","Clone method [Security]","Clone method [Security]","IEnumCERTVIEWATTRIBUTE interface","IEnumCERTVIEWATTRIBUTE interface [Security]","Clone method","IEnumCERTVIEWATTRIBUTE.Clone","IEnumCERTVIEWATTRIBUTE::Clone","_certsrv_ienumcertviewattribute_clone","certview/IEnumCERTVIEWATTRIBUTE::Clone","security.ienumcertviewattribute_clone"]
old-location: security\ienumcertviewattribute_clone.htm
tech.root: security
ms.assetid: 6144514a-cd64-42ce-a856-ff942b129e5a
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Security], Clone method [Security],IEnumCERTVIEWATTRIBUTE interface, IEnumCERTVIEWATTRIBUTE interface [Security],Clone method, IEnumCERTVIEWATTRIBUTE.Clone, IEnumCERTVIEWATTRIBUTE::Clone, _certsrv_ienumcertviewattribute_clone, certview/IEnumCERTVIEWATTRIBUTE::Clone, security.ienumcertviewattribute_clone
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
 - IEnumCERTVIEWATTRIBUTE::Clone
 - certview/IEnumCERTVIEWATTRIBUTE::Clone
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
 - IEnumCERTVIEWATTRIBUTE.Clone
 - IEnumCERTVIEWATTRIBUTE.Clone
---

# IEnumCERTVIEWATTRIBUTE::Clone


## -description

The <b>Clone</b> method creates a copy of the attribute-enumeration sequence object in its current state.

## -parameters

### -param ppenum [out]

A pointer to a pointer of <a href="/windows/desktop/api/certview/nn-certview-ienumcertviewattribute">IEnumCERTVIEWATTRIBUTE</a> type. This function will fail if <i>ppenum</i> is <b>NULL</b>.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a cloned attribute-enumeration sequence object.

## -remarks

The attribute-enumeration sequence object is obtained by a call to 
the <a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-enumcertviewattribute">IEnumCERTVIEWROW::EnumCertViewAttribute</a> method.


#### Examples


```cpp
// pEnumAttr is previously instantiated IEnumCERTVIEWATTRIBUTE object
IEnumCERTVIEWATTRIBUTE * pEnumAttr2 = NULL;
HRESULT    hr;
hr = pEnumAttr->Clone(&pEnumAttr2);
if (S_OK != hr)
    printf("Unable to clone IEnumCERTVIEWATTRIBUTE\n");
else
{
    // use cloned object as needed
    // ...
}
// done using cloned object, free memory
if (NULL != pEnumAttr2)
    pEnumAttr2->Release();
```

## -see-also

<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewattribute">IEnumCERTVIEWATTRIBUTE</a>