---
UID: NF:certview.IEnumCERTVIEWCOLUMN.Skip
title: IEnumCERTVIEWCOLUMN::Skip (certview.h)
description: Skips a specified number of columns in the column-enumeration sequence.
helpviewer_keywords: ["IEnumCERTVIEWCOLUMN interface [Security]","Skip method","IEnumCERTVIEWCOLUMN object [Security]","Skip method","IEnumCERTVIEWCOLUMN.Skip","IEnumCERTVIEWCOLUMN::Skip","Skip","Skip method [Security]","Skip method [Security]","IEnumCERTVIEWCOLUMN interface","Skip method [Security]","IEnumCERTVIEWCOLUMN object","_certsrv_ienumcertviewcolumn_skip","certview/IEnumCERTVIEWCOLUMN::Skip","security.ienumcertviewcolumn_skip"]
old-location: security\ienumcertviewcolumn_skip.htm
tech.root: security
ms.assetid: 9a101e5b-a137-4e15-81b6-90e0fc14b887
ms.date: 12/05/2018
ms.keywords: IEnumCERTVIEWCOLUMN interface [Security],Skip method, IEnumCERTVIEWCOLUMN object [Security],Skip method, IEnumCERTVIEWCOLUMN.Skip, IEnumCERTVIEWCOLUMN::Skip, Skip, Skip method [Security], Skip method [Security],IEnumCERTVIEWCOLUMN interface, Skip method [Security],IEnumCERTVIEWCOLUMN object, _certsrv_ienumcertviewcolumn_skip, certview/IEnumCERTVIEWCOLUMN::Skip, security.ienumcertviewcolumn_skip
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
 - IEnumCERTVIEWCOLUMN::Skip
 - certview/IEnumCERTVIEWCOLUMN::Skip
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
 - IEnumCERTVIEWCOLUMN.Skip
 - IEnumCERTVIEWCOLUMN.Skip
---

# IEnumCERTVIEWCOLUMN::Skip


## -description

The <b>Skip</b> method skips a specified number of columns in the column-enumeration sequence.

## -parameters

### -param celt [in]

The number of columns to skip. A positive value for the <i>celt</i> parameter causes the column-enumeration sequence to skip forward in the enumeration sequence. A negative value causes column-enumeration to skip backward in the enumeration sequence.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

A return value of E_INVALIDARG indicates that a negative value in the   <i>celt</i> parameter caused the column-enumeration sequence index to become less than zero.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Upon successful completion of this function, call the 
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-next">IEnumCERTVIEWCOLUMN::Next</a> method to reference the current column in the column-enumeration sequence. After this second call is made, the information in the column can be obtained by calling one of the following methods:

<ul>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-getname">IEnumCERTVIEWCOLUMN::GetName</a>: Retrieves the nonlocalized name of the column.</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-getdisplayname">IEnumCERTVIEWCOLUMN::GetDisplayName</a>: Retrieves the localized name of the column.</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-getvalue">IEnumCERTVIEWCOLUMN::GetValue</a>: Retrieves the data in the column.</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-gettype">IEnumCERTVIEWCOLUMN::GetType</a>: Retrieves the type of data in the column.</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-getmaxlength">IEnumCERTVIEWCOLUMN::GetMaxLength</a>: Retrieves the maximum length, in bytes, of the column.</li>
</ul>
The column-enumeration sequence maintains an internal  zero-based index. The call to the <b>Skip</b> method causes this index to increase or decrease based on the setting of the <i>celt</i> parameter.

If a negative value of the <i>celt</i> parameter causes the index to be less than zero, the behavior of subsequent calls to <a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-next">Next</a> is undefined.

If a positive value of the <i>celt</i> parameter causes the index to exceed the last row in the enumeration sequence, a subsequent call to the <a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-next">Next</a> method will fail.


#### Examples


```cpp
HRESULT  hr;
LONG     Index;

// pEnumCol is previously instantiated IEnumCERTVIEWCOLUMN object
// skip the next five columns
hr = pEnumCol->Skip(5);
if (S_OK == hr) 
{
    // get the next column
    hr = pEnumCol->Next(&Index);
    if (S_OK == hr)
    {
        // Use this column as needed.
    }
}
```

## -see-also

<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewcolumn">IEnumCERTVIEWCOLUMN</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-reset">IEnumCERTVIEWCOLUMN::Reset</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-next">IEnumCERTVIEWCOLUMN:Next</a>