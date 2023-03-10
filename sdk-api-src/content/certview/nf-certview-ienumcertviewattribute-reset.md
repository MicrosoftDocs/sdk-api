---
UID: NF:certview.IEnumCERTVIEWATTRIBUTE.Reset
title: IEnumCERTVIEWATTRIBUTE::Reset (certview.h)
description: Moves to the beginning of the attribute-enumeration sequence.
helpviewer_keywords: ["CEnumCERTVIEWATTRIBUTE object [Security]","Reset method","IEnumCERTVIEWATTRIBUTE interface [Security]","Reset method","IEnumCERTVIEWATTRIBUTE.Reset","IEnumCERTVIEWATTRIBUTE::Reset","Reset","Reset method [Security]","Reset method [Security]","CEnumCERTVIEWATTRIBUTE object","Reset method [Security]","IEnumCERTVIEWATTRIBUTE interface","_certsrv_ienumcertviewattribute_reset","certview/IEnumCERTVIEWATTRIBUTE::Reset","security.ienumcertviewattribute_reset"]
old-location: security\ienumcertviewattribute_reset.htm
tech.root: security
ms.assetid: 1f5b8ee0-2820-481b-8836-b2926aec0933
ms.date: 12/05/2018
ms.keywords: CEnumCERTVIEWATTRIBUTE object [Security],Reset method, IEnumCERTVIEWATTRIBUTE interface [Security],Reset method, IEnumCERTVIEWATTRIBUTE.Reset, IEnumCERTVIEWATTRIBUTE::Reset, Reset, Reset method [Security], Reset method [Security],CEnumCERTVIEWATTRIBUTE object, Reset method [Security],IEnumCERTVIEWATTRIBUTE interface, _certsrv_ienumcertviewattribute_reset, certview/IEnumCERTVIEWATTRIBUTE::Reset, security.ienumcertviewattribute_reset
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
 - IEnumCERTVIEWATTRIBUTE::Reset
 - certview/IEnumCERTVIEWATTRIBUTE::Reset
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
 - IEnumCERTVIEWATTRIBUTE.Reset
 - CEnumCERTVIEWATTRIBUTE.Reset
---

# IEnumCERTVIEWATTRIBUTE::Reset


## -description

The <b>Reset</b> method moves to the beginning of the attribute-enumeration sequence.



## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Upon successful completion of this method, call the 
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-next">IEnumCERTVIEWATTRIBUTE::Next</a> method to reference the first attribute in the attribute-enumeration sequence.  The attribute name and value can be accessed by using the 
following methods:

<ul>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-getname">IEnumCERTVIEWATTRIBUTE::GetName</a>
</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-getvalue">IEnumCERTVIEWATTRIBUTE::GetValue</a>
</li>
</ul>

#### Examples


```cpp
// pEnumAttr is a previously instantiated
// IEnumCERTVIEWATTRIBUTE object.
HRESULT  hr;
LONG     Index;

hr = pEnumAttr->Reset();
if (S_OK != hr)
    printf("Unable to reset pEnumAttr - %x\n", hr );


    // Call the appropriate error handler and exit routine.
else
{

    // Reset to the beginning of the attributes again.
    while (S_OK == pEnumAttr->Next(&Index))
    {

        // Use each attribute as needed.
    }
}
```

## -see-also

<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewattribute">IEnumCERTVIEWATTRIBUTE</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-getname">IEnumCERTVIEWATTRIBUTE::GetName</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-getvalue">IEnumCERTVIEWATTRIBUTE::GetValue</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-next">IEnumCERTVIEWATTRIBUTE::Next</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-skip">IEnumCERTVIEWATTRIBUTE::Skip</a>
