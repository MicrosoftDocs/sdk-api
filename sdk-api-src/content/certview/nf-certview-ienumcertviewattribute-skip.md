---
UID: NF:certview.IEnumCERTVIEWATTRIBUTE.Skip
title: IEnumCERTVIEWATTRIBUTE::Skip (certview.h)
description: Skips a specified number of attributes in the attribute-enumeration sequence.
helpviewer_keywords: ["IEnumCERTVIEWATTRIBUTE interface [Security]","Skip method","IEnumCERTVIEWATTRIBUTE object [Security]","Skip method","IEnumCERTVIEWATTRIBUTE.Skip","IEnumCERTVIEWATTRIBUTE::Skip","Skip","Skip method [Security]","Skip method [Security]","IEnumCERTVIEWATTRIBUTE interface","Skip method [Security]","IEnumCERTVIEWATTRIBUTE object","_certsrv_ienumcertviewattribute_skip","certview/IEnumCERTVIEWATTRIBUTE::Skip","security.ienumcertviewattribute_skip"]
old-location: security\ienumcertviewattribute_skip.htm
tech.root: security
ms.assetid: 546e7ad7-73f2-4f6e-8d02-a9ca5401ecce
ms.date: 12/05/2018
ms.keywords: IEnumCERTVIEWATTRIBUTE interface [Security],Skip method, IEnumCERTVIEWATTRIBUTE object [Security],Skip method, IEnumCERTVIEWATTRIBUTE.Skip, IEnumCERTVIEWATTRIBUTE::Skip, Skip, Skip method [Security], Skip method [Security],IEnumCERTVIEWATTRIBUTE interface, Skip method [Security],IEnumCERTVIEWATTRIBUTE object, _certsrv_ienumcertviewattribute_skip, certview/IEnumCERTVIEWATTRIBUTE::Skip, security.ienumcertviewattribute_skip
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
 - IEnumCERTVIEWATTRIBUTE::Skip
 - certview/IEnumCERTVIEWATTRIBUTE::Skip
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
 - IEnumCERTVIEWATTRIBUTE.Skip
 - IEnumCERTVIEWATTRIBUTE.Skip
---

# IEnumCERTVIEWATTRIBUTE::Skip


## -description

The <b>Skip</b> method skips a specified number of attributes in the attribute-enumeration sequence.

## -parameters

### -param celt [in]

The number of attributes to skip. A positive value for the <i>celt</i> parameter  causes the attribute-enumeration sequence to skip forward in the sequence. A negative value for the <i>celt</i> parameter causes the attribute-enumeration sequence to skip backward in the sequence.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

A return value of E_INVALIDARG indicates that a negative value for the <i>celt</i> parameter caused the attribute-enumeration sequence index to become less than zero.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Upon successful completion of this method, call the 
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-next">IEnumCERTVIEWATTRIBUTE::Next</a> method to reference the current attribute in the attribute-enumeration sequence.  The attribute name and value can be accessed through the 
following methods:

<ul>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-getname">IEnumCERTVIEWATTRIBUTE::GetName</a>
</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-getvalue">IEnumCERTVIEWATTRIBUTE::GetValue</a>
</li>
</ul>
The attribute-enumeration sequence maintains an internal  zero-based index. The call to the <a href="/windows/desktop/api/certview/nn-certview-ienumcertviewattribute">Skip</a> method causes this index to increase or decrease by the number of attributes specified in the  <i>celt</i> parameter.

If a negative value of the <i>celt</i> parameter causes the index to be less than zero, the behavior of subsequent calls to <a href="/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-next">IEnumCERTVIEWATTRIBUTE::Next</a> is undefined.

If a positive value of the <i>celt</i> parameter causes the  index to exceed the last attribute in the enumeration sequence, a subsequent call to the <a href="/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-next">IEnumCERTVIEWATTRIBUTE::Next</a> method will fail.


#### Examples


```cpp
HRESULT  hr;
LONG     Index;

// pEnumAttr is previously instantiated IEnumCERTVIEWATTRIBUTE object
// skip the next 5 attributes
hr = pEnumAttr->Skip(5);
if (S_OK == hr)
{
    // get the next attribute
    hr = pEnumAttr->Next(&Index);
    if (S_OK == hr)
    {
        // Use this attribute as needed.
    }
}
```

## -see-also

<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewattribute">IEnumCERTVIEWATTRIBUTE</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-reset">IEnumCERTVIEWATTRIBUTE::Reset</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-next">IEnumCERTVIEWATTRIBUTE:Next</a>