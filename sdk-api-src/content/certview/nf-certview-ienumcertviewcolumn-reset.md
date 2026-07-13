---
UID: NF:certview.IEnumCERTVIEWCOLUMN.Reset
title: IEnumCERTVIEWCOLUMN::Reset (certview.h)
description: Moves to the beginning of the column-enumeration sequence.
helpviewer_keywords: ["IEnumCERTVIEWCOLUMN interface [Security]","Reset method","IEnumCERTVIEWCOLUMN object [Security]","Reset method","IEnumCERTVIEWCOLUMN.Reset","IEnumCERTVIEWCOLUMN::Reset","Reset","Reset method [Security]","Reset method [Security]","IEnumCERTVIEWCOLUMN interface","Reset method [Security]","IEnumCERTVIEWCOLUMN object","_certsrv_ienumcertviewcolumn_reset","certview/IEnumCERTVIEWCOLUMN::Reset","security.ienumcertviewcolumn_reset"]
old-location: security\ienumcertviewcolumn_reset.htm
tech.root: security
ms.assetid: 0be00eb0-1a22-4849-95ca-276099bbfa74
ms.date: 12/05/2018
ms.keywords: IEnumCERTVIEWCOLUMN interface [Security],Reset method, IEnumCERTVIEWCOLUMN object [Security],Reset method, IEnumCERTVIEWCOLUMN.Reset, IEnumCERTVIEWCOLUMN::Reset, Reset, Reset method [Security], Reset method [Security],IEnumCERTVIEWCOLUMN interface, Reset method [Security],IEnumCERTVIEWCOLUMN object, _certsrv_ienumcertviewcolumn_reset, certview/IEnumCERTVIEWCOLUMN::Reset, security.ienumcertviewcolumn_reset
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
 - IEnumCERTVIEWCOLUMN::Reset
 - certview/IEnumCERTVIEWCOLUMN::Reset
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
 - IEnumCERTVIEWCOLUMN.Reset
 - IEnumCERTVIEWCOLUMN.Reset
---

# IEnumCERTVIEWCOLUMN::Reset


## -description

The <b>Reset</b> method moves to the beginning of the column-enumeration sequence.



## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Upon successful completion of this method, call the 
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-next">IEnumCERTVIEWCOLUMN::Next</a> method to reference the first column in the enumeration. After this second call is made, the information in the column can be obtained by calling one of the following methods:

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

#### Examples


```cpp
// pEnumCol is previously instantiated IEnumCERTVIEWCOLUMN object
HRESULT    hr;
LONG        Index;
hr = pEnumCol->Reset();
if (S_OK != hr)
    printf("Unable to reset pEnumCol\n");
    // call appropriate error handler / exit routine
else
{
    // now at the beginning of the columns
    // enumerate each column
    while (S_OK == pEnumCol->Next(&Index))
    {
        // Use each column as needed.
    }
}
```

## -see-also

<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewcolumn">IEnumCERTVIEWCOLUMN</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-getdisplayname">IEnumCERTVIEWCOLUMN::GetDisplayName</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-getmaxlength">IEnumCERTVIEWCOLUMN::GetMaxLength</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-getname">IEnumCERTVIEWCOLUMN::GetName</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-gettype">IEnumCERTVIEWCOLUMN::GetType</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-getvalue">IEnumCERTVIEWCOLUMN::GetValue</a>
