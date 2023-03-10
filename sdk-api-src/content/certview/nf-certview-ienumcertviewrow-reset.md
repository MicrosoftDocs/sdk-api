---
UID: NF:certview.IEnumCERTVIEWROW.Reset
title: IEnumCERTVIEWROW::Reset (certview.h)
description: Moves to the beginning of the row-enumeration sequence.
helpviewer_keywords: ["IEnumCERTVIEWROW interface [Security]","Reset method","IEnumCERTVIEWROW object [Security]","Reset method","IEnumCERTVIEWROW.Reset","IEnumCERTVIEWROW::Reset","Reset","Reset method [Security]","Reset method [Security]","IEnumCERTVIEWROW interface","Reset method [Security]","IEnumCERTVIEWROW object","_certsrv_ienumcertviewrow_reset","certview/IEnumCERTVIEWROW::Reset","security.ienumcertviewrow_reset"]
old-location: security\ienumcertviewrow_reset.htm
tech.root: security
ms.assetid: 76bee5db-0443-4673-a59c-0198587736dc
ms.date: 12/05/2018
ms.keywords: IEnumCERTVIEWROW interface [Security],Reset method, IEnumCERTVIEWROW object [Security],Reset method, IEnumCERTVIEWROW.Reset, IEnumCERTVIEWROW::Reset, Reset, Reset method [Security], Reset method [Security],IEnumCERTVIEWROW interface, Reset method [Security],IEnumCERTVIEWROW object, _certsrv_ienumcertviewrow_reset, certview/IEnumCERTVIEWROW::Reset, security.ienumcertviewrow_reset
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
 - IEnumCERTVIEWROW::Reset
 - certview/IEnumCERTVIEWROW::Reset
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
 - IEnumCERTVIEWROW.Reset
 - IEnumCERTVIEWROW.Reset
---

# IEnumCERTVIEWROW::Reset


## -description

The <b>Reset</b> method moves to the beginning of the row-enumeration sequence.



## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Upon successful completion of this method, call the <a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-next">IEnumCERTVIEWROW::Next</a> method to reference the first row in the enumeration. 

After this second call is made, the 
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

#### Examples


```cpp
// pEnumRow is previously instantiated pointer to IEnumCERTVIEWROW.
HRESULT hr;
LONG    Index;

// Ensure enumerator is at first row.
hr = pEnumRow->Reset();
if (FAILED(hr))
    printf("Failed to Reset\n");
else
{
    printf("Reset to beginning\n");
    // Retrieve first record.
    hr = pEnumRow->Next(&Index);
    // Examine hr for success and process row.
    // ...
}
```

## -see-also

<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewattribute">IEnumCERTVIEWATTRIBUTE</a>



<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewcolumn">IEnumCERTVIEWCOLUMN</a>



<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewextension">IEnumCERTVIEWEXTENSION</a>



<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewrow">IEnumCERTVIEWROW</a>
