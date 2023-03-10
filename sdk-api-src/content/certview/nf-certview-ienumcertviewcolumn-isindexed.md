---
UID: NF:certview.IEnumCERTVIEWCOLUMN.IsIndexed
title: IEnumCERTVIEWCOLUMN::IsIndexed (certview.h)
description: Reports whether the data in the column is indexed.
helpviewer_keywords: ["IEnumCERTVIEWCOLUMN interface [Security]","IsIndexed method","IEnumCERTVIEWCOLUMN.IsIndexed","IEnumCERTVIEWCOLUMN::IsIndexed","IsIndexed","IsIndexed method [Security]","IsIndexed method [Security]","IEnumCERTVIEWCOLUMN interface","_certsrv_ienumcertviewcolumn_isindexed","certview/IEnumCERTVIEWCOLUMN::IsIndexed","security.ienumcertviewcolumn_isindexed"]
old-location: security\ienumcertviewcolumn_isindexed.htm
tech.root: security
ms.assetid: 7373c0c3-3a1d-4a32-90e6-0f0575a0b61b
ms.date: 12/05/2018
ms.keywords: IEnumCERTVIEWCOLUMN interface [Security],IsIndexed method, IEnumCERTVIEWCOLUMN.IsIndexed, IEnumCERTVIEWCOLUMN::IsIndexed, IsIndexed, IsIndexed method [Security], IsIndexed method [Security],IEnumCERTVIEWCOLUMN interface, _certsrv_ienumcertviewcolumn_isindexed, certview/IEnumCERTVIEWCOLUMN::IsIndexed, security.ienumcertviewcolumn_isindexed
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
 - IEnumCERTVIEWCOLUMN::IsIndexed
 - certview/IEnumCERTVIEWCOLUMN::IsIndexed
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
 - IEnumCERTVIEWCOLUMN.IsIndexed
 - IEnumCERTVIEWCOLUMN.IsIndexed
---

# IEnumCERTVIEWCOLUMN::IsIndexed


## -description

The <b>IsIndexed</b> method reports whether the data in the column is indexed.

## -parameters

### -param pIndexed [out]

A pointer to a variable of type <b>LONG</b> that indicates <b>TRUE</b> if the data is indexed and <b>FALSE</b> if the data is not indexed. This method fails if <i>pIndexed</i> is set to <b>NULL</b>.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK and the <i>pIndexed</i> is set to <b>TRUE</b> or <b>FALSE</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 One if the column is indexed; otherwise, zero.

## -remarks

This method is used to determine whether the data of the current column referenced by the column-enumeration sequence is indexed.

If the column-enumeration sequence is not referencing a valid column, <b>IsIndexed</b> will fail. Use one of the following methods to navigate through the enumeration:

<ul>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-reset">IEnumCERTVIEWCOLUMN::Reset</a>: Moves to the beginning of the enumeration sequence.</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-next">IEnumCERTVIEWCOLUMN::Next</a>: Moves to the next column in the enumeration sequence.</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-skip">IEnumCERTVIEWCOLUMN::Skip</a>: Skips a specified number of columns.</li>
</ul>

#### Examples


```cpp
HRESULT  hr;
LONG     bIsindexed;

// pEnumCol is previously instantiated IEnumCERTVIEWCOLUMN object
hr = pEnumCol->IsIndexed(&bIsindexed);
if (S_OK == hr)
    printf( bIsindexed ? "Indexed\n" : "Not indexed\n");
```

## -see-also

<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewcolumn">IEnumCERTVIEWCOLUMN</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-next">IEnumCERTVIEWCOLUMN::Next</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-reset">IEnumCERTVIEWCOLUMN::Reset</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-skip">IEnumCERTVIEWCOLUMN::Skip</a>