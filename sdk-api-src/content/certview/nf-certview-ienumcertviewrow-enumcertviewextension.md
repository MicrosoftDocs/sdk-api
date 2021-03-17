---
UID: NF:certview.IEnumCERTVIEWROW.EnumCertViewExtension
title: IEnumCERTVIEWROW::EnumCertViewExtension (certview.h)
description: Obtains an instance of an extension-enumeration sequence for the current row of the row-enumeration sequence.
helpviewer_keywords: ["EnumCertViewExtension","EnumCertViewExtension method [Security]","EnumCertViewExtension method [Security]","IEnumCERTVIEWROW interface","IEnumCERTVIEWROW interface [Security]","EnumCertViewExtension method","IEnumCERTVIEWROW.EnumCertViewExtension","IEnumCERTVIEWROW::EnumCertViewExtension","_certsrv_ienumcertviewrow_enumcertviewextension","certview/IEnumCERTVIEWROW::EnumCertViewExtension","security.ienumcertviewrow_enumcertviewextension"]
old-location: security\ienumcertviewrow_enumcertviewextension.htm
tech.root: security
ms.assetid: 41028000-fa87-4ad0-93fc-314c5d3870f9
ms.date: 12/05/2018
ms.keywords: EnumCertViewExtension, EnumCertViewExtension method [Security], EnumCertViewExtension method [Security],IEnumCERTVIEWROW interface, IEnumCERTVIEWROW interface [Security],EnumCertViewExtension method, IEnumCERTVIEWROW.EnumCertViewExtension, IEnumCERTVIEWROW::EnumCertViewExtension, _certsrv_ienumcertviewrow_enumcertviewextension, certview/IEnumCERTVIEWROW::EnumCertViewExtension, security.ienumcertviewrow_enumcertviewextension
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
 - IEnumCERTVIEWROW::EnumCertViewExtension
 - certview/IEnumCERTVIEWROW::EnumCertViewExtension
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
 - IEnumCERTVIEWROW.EnumCertViewExtension
 - IEnumCERTVIEWROW.EnumCertViewExtension
---

# IEnumCERTVIEWROW::EnumCertViewExtension


## -description

The <b>EnumCertViewExtension</b> method obtains an instance of an extension-enumeration sequence for the current row of the row-enumeration sequence.

## -parameters

### -param Flags [in]

<table>
<tr>
<td><strong>C++</strong></td>
<td>
A <b>LONG</b> value. Must be zero.

</td>
</tr>
<tr>
<td><strong>VB</strong></td>
<td>
A <b>Long</b> value. Must be zero.

</td>
</tr>
</table>

### -param ppenum [out, retval]

A pointer to a pointer of <a href="/windows/desktop/api/certview/nn-certview-ienumcertviewextension">IEnumCERTVIEWEXTENSION</a> type.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is an extension-enumeration sequence object.

## -remarks

The 
extension-enumeration sequence obtained by this call can be used to enumerate the extensions associated with the certificate in the current row. This enumeration can be accessed through the methods of the <a href="/windows/desktop/api/certview/nn-certview-ienumcertviewextension">IEnumCERTVIEWEXTENSION</a> interface.

To reference a different row, call one of the following methods to navigate through the row-enumeration sequence:

<ul>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-reset">IEnumCERTVIEWROW::Reset</a>: Moves to the beginning of the enumeration sequence.</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-next">IEnumCERTVIEWROW::Next</a>: Moves to the next row in the enumeration sequence.</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-skip">IEnumCERTVIEWROW::Skip</a>: Skips a specified number of rows.</li>
</ul>

#### Examples


```cpp
// pEnumRow is previously instantiated pointer to IEnumCERTVIEWROW.
LONG       Index;
HRESULT    hr;
IEnumCERTVIEWEXTENSION * pEnumExt = NULL;
// Obtain enumerator for extensions.
hr = pEnumRow->EnumCertViewExtension(0, &pEnumExt);
if (FAILED(hr))
{
    printf("Failed EnumCertViewExtension - %x\n", hr);
    goto error;
}
// Enumerate each extension.
while (S_OK == pEnumExt->Next(&Index))
{
    // Use this extension as needed.
}
error:

// Free resources.
if (NULL != pEnumExt)
    pEnumExt->Release();
```

## -see-also

<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewextension">IEnumCERTVIEWEXTENSION</a>



<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewrow">IEnumCERTVIEWROW</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-next">IEnumCERTVIEWROW::Next</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-reset">IEnumCERTVIEWROW::Reset</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-skip">IEnumCERTVIEWROW::Skip</a>