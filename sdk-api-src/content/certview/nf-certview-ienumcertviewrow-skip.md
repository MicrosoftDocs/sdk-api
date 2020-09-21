---
UID: NF:certview.IEnumCERTVIEWROW.Skip
title: IEnumCERTVIEWROW::Skip (certview.h)
description: Skips a specified number of rows in the row enumeration sequence.
helpviewer_keywords: ["IEnumCERTVIEWROW interface [Security]","Skip method","IEnumCERTVIEWROW object [Security]","Skip method","IEnumCERTVIEWROW.Skip","IEnumCERTVIEWROW::Skip","Skip","Skip method [Security]","Skip method [Security]","IEnumCERTVIEWROW interface","Skip method [Security]","IEnumCERTVIEWROW object","_certsrv_ienumcertviewrow_skip","certview/IEnumCERTVIEWROW::Skip","security.ienumcertviewrow_skip"]
old-location: security\ienumcertviewrow_skip.htm
tech.root: security
ms.assetid: 9115262e-00bb-4446-906d-7a57fd5781d1
ms.date: 12/05/2018
ms.keywords: IEnumCERTVIEWROW interface [Security],Skip method, IEnumCERTVIEWROW object [Security],Skip method, IEnumCERTVIEWROW.Skip, IEnumCERTVIEWROW::Skip, Skip, Skip method [Security], Skip method [Security],IEnumCERTVIEWROW interface, Skip method [Security],IEnumCERTVIEWROW object, _certsrv_ienumcertviewrow_skip, certview/IEnumCERTVIEWROW::Skip, security.ienumcertviewrow_skip
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
 - IEnumCERTVIEWROW::Skip
 - certview/IEnumCERTVIEWROW::Skip
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
 - IEnumCERTVIEWROW.Skip
 - IEnumCERTVIEWROW.Skip
---

# IEnumCERTVIEWROW::Skip


## -description

The <b>Skip</b> method skips a specified number of rows in the 
row enumeration sequence.

## -parameters

### -param celt [in]

The number of rows to skip. A positive value for the <i>celt</i> parameter causes the row-enumeration sequence to skip forward in the enumeration sequence. A negative value for the <i>celt</i> parameter causes the row enumeration sequence to skip backward in the enumeration sequence.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

A return value of E_INVALIDARG indicates that the <i>celt</i> parameter was set to a negative number which caused the row-enumeration sequence  index to become less than zero.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Upon successful completion of this method, call  the 
<b>IEnumCERTVIEWROW::Skip</b> method to reference the current row in the row-enumeration sequence. After this second call is made, the 
columns, attributes, and extensions associated with the certificate in the row can be enumerated using the methods of the following interfaces:

<ul>
<li>
<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewcolumn">IEnumCERTVIEWCOLUMN</a>
</li>
<li>
<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewattribute">IEnumCERTVIEWATTRIBUTE</a>
</li>
<li>
<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewextension">IEnumCERTVIEWEXTENSION</a>
</li>
</ul>
The row-enumeration sequence maintains an internal  zero-based index. The call to the <b>Skip</b> method causes this index to increase or decrease based on the setting of the <i>celt</i> parameter.

If a negative value of the <i>celt</i> parameter causes the index to be less than zero, the behavior of subsequent calls to <a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-next">Next</a> is undefined.

If a positive value of the <i>celt</i> parameter causes the index to exceed the last row in the enumeration sequence, a subsequent call to the <a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-next">Next</a> method will fail.


#### Examples


```cpp
// pEnumRow is previously instantiated pointer to IEnumCERTVIEWROW.
HRESULT  hr;
LONG     Index;
// Reposition the row enumerator to the beginning of the rows.
hr = pEnumRow->Reset();
if (FAILED(hr))
{
    printf("Unable to reset pEnumRow\n");
    goto error;
}
// Skip some rows.
hr = pEnumRow->Skip(5);
if (FAILED(hr))
{
    printf("Unable to skip rows\n");
    goto error;
}

// Get the next row.
hr = pEnumRow->Next(&Index);
if (S_OK == hr)
{
    // Use this row as needed.
}

error:

if (NULL != pEnumRow)
    pEnumRow->Release();
```

## -see-also

<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewattribute">IEnumCERTVIEWATTRIBUTE</a>



<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewcolumn">IEnumCERTVIEWCOLUMN</a>



<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewextension">IEnumCERTVIEWEXTENSION</a>



<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewrow">IEnumCERTVIEWROW</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-next">IEnumCERTVIEWROW::Next</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-reset">IEnumCERTVIEWROW::Reset</a>