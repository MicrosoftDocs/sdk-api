---
UID: NF:certview.IEnumCERTVIEWCOLUMN.Clone
title: IEnumCERTVIEWCOLUMN::Clone (certview.h)
description: Creates a copy of the column-enumeration sequence.
helpviewer_keywords: ["Clone","Clone method [Security]","Clone method [Security]","IEnumCERTVIEWCOLUMN interface","IEnumCERTVIEWCOLUMN interface [Security]","Clone method","IEnumCERTVIEWCOLUMN.Clone","IEnumCERTVIEWCOLUMN::Clone","_certsrv_ienumcertviewcolumn_clone","certview/IEnumCERTVIEWCOLUMN::Clone","security.ienumcertviewcolumn_clone"]
old-location: security\ienumcertviewcolumn_clone.htm
tech.root: security
ms.assetid: a0870155-3f16-4cfb-b180-7a8e617dfcd8
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Security], Clone method [Security],IEnumCERTVIEWCOLUMN interface, IEnumCERTVIEWCOLUMN interface [Security],Clone method, IEnumCERTVIEWCOLUMN.Clone, IEnumCERTVIEWCOLUMN::Clone, _certsrv_ienumcertviewcolumn_clone, certview/IEnumCERTVIEWCOLUMN::Clone, security.ienumcertviewcolumn_clone
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
 - IEnumCERTVIEWCOLUMN::Clone
 - certview/IEnumCERTVIEWCOLUMN::Clone
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
 - IEnumCERTVIEWCOLUMN.Clone
 - IEnumCERTVIEWCOLUMN.Clone
---

# IEnumCERTVIEWCOLUMN::Clone


## -description

The <b>Clone</b> method creates a copy of the column-enumeration sequence.

## -parameters

### -param ppenum [out]

A pointer to a pointer of <a href="/windows/desktop/api/certview/nn-certview-ienumcertviewcolumn">IEnumCERTVIEWCOLUMN</a> type. This method will fail if the <i>ppenum</i> is <b>NULL</b>.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a cloned column-enumeration sequence object.

## -remarks

The column-enumeration sequence is obtained by a call to the <a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-enumcertviewcolumn">IEnumCERTVIEWROW::EnumCertViewColumn</a> method.


#### Examples


```cpp
// pEnumCol is previously instantiated IEnumCERTVIEWCOLUMN object
IEnumCERTVIEWCOLUMN * pEnumCol2 = NULL;
HRESULT    hr;
hr = pEnumCol->Clone(&pEnumCol2);
if (S_OK != hr)
    printf("Unable to clone IEnumCERTVIEWCOLUMN\n");
else
{
    // use cloned object as needed
    // ...
    // done using cloned object, free memory
}
if (NULL != pEnumCol2)
    pEnumCol2->Release();
```

## -see-also

<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewcolumn">IEnumCERTVIEWCOLUMN</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-enumcertviewcolumn">IEnumCERTVIEWROW::EnumCertViewColumn</a>