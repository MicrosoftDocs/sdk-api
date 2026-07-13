---
UID: NF:certview.IEnumCERTVIEWEXTENSION.Reset
title: IEnumCERTVIEWEXTENSION::Reset (certview.h)
description: Moves to the beginning of the extension-enumeration sequence.
helpviewer_keywords: ["IEnumCERTVIEWEXTENSION interface [Security]","Reset method","IEnumCERTVIEWEXTENSION object [Security]","Reset method","IEnumCERTVIEWEXTENSION.Reset","IEnumCERTVIEWEXTENSION::Reset","Reset","Reset method [Security]","Reset method [Security]","IEnumCERTVIEWEXTENSION interface","Reset method [Security]","IEnumCERTVIEWEXTENSION object","_certsrv_ienumcertviewextension_reset","certview/IEnumCERTVIEWEXTENSION::Reset","security.ienumcertviewextension_reset"]
old-location: security\ienumcertviewextension_reset.htm
tech.root: security
ms.assetid: 7af29b1f-5b43-4ab7-81fa-d03e065f014f
ms.date: 12/05/2018
ms.keywords: IEnumCERTVIEWEXTENSION interface [Security],Reset method, IEnumCERTVIEWEXTENSION object [Security],Reset method, IEnumCERTVIEWEXTENSION.Reset, IEnumCERTVIEWEXTENSION::Reset, Reset, Reset method [Security], Reset method [Security],IEnumCERTVIEWEXTENSION interface, Reset method [Security],IEnumCERTVIEWEXTENSION object, _certsrv_ienumcertviewextension_reset, certview/IEnumCERTVIEWEXTENSION::Reset, security.ienumcertviewextension_reset
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
 - IEnumCERTVIEWEXTENSION::Reset
 - certview/IEnumCERTVIEWEXTENSION::Reset
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
 - IEnumCERTVIEWEXTENSION.Reset
 - IEnumCERTVIEWEXTENSION.Reset
---

# IEnumCERTVIEWEXTENSION::Reset


## -description

The <b>Reset</b> method moves to the beginning of the extension-enumeration sequence.



## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Upon successful completion of this method, call the 
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-next">IEnumCERTVIEWEXTENSION::Next</a> method to reference the first extension in the extension-enumeration sequence.

The extension name, flags, and value can be accessed through 
the following methods:

<ul>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-getname">IEnumCERTVIEWEXTENSION::GetName</a>
</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-getflags">IEnumCERTVIEWEXTENSION::GetFlags</a>
</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-getvalue">IEnumCERTVIEWEXTENSION::GetValue</a>
</li>
</ul>

#### Examples


```cpp
HRESULT  hr;
LONG     Index;

// pEnumExt is previously instantiated IEnumCERTVIEWEXTENSION object
hr = pEnumExt->Reset();
if (S_OK != hr)
    printf("Unable to reset pEnumExt - %x\n", hr);
    // call appropriate error handler / exit routine
else
{
    // reset to beginning of extensions again
    while (S_OK == pEnumExt->Next(&Index))
    {
        // Use each extension as needed.
    }
}
```

## -see-also

<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewextension">IEnumCERTVIEWEXTENSION</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-getflags">IEnumCERTVIEWEXTENSION::GetFlags</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-getname">IEnumCERTVIEWEXTENSION::GetName</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-getvalue">IEnumCERTVIEWEXTENSION::GetValue</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-next">IEnumCERTVIEWEXTENSION::Next</a>
