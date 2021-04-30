---
UID: NF:certview.IEnumCERTVIEWCOLUMN.GetMaxLength
title: IEnumCERTVIEWCOLUMN::GetMaxLength (certview.h)
description: Retrieves the maximum allowable length, in bytes, for the column data.
helpviewer_keywords: ["GetMaxLength","GetMaxLength method [Security]","GetMaxLength method [Security]","IEnumCERTVIEWCOLUMN interface","IEnumCERTVIEWCOLUMN interface [Security]","GetMaxLength method","IEnumCERTVIEWCOLUMN.GetMaxLength","IEnumCERTVIEWCOLUMN::GetMaxLength","_certsrv_ienumcertviewcolumn_getmaxlength","certview/IEnumCERTVIEWCOLUMN::GetMaxLength","security.ienumcertviewcolumn_getmaxlength"]
old-location: security\ienumcertviewcolumn_getmaxlength.htm
tech.root: security
ms.assetid: 20cd5f5a-2e19-43ca-9b84-70e6dd1a4cad
ms.date: 12/05/2018
ms.keywords: GetMaxLength, GetMaxLength method [Security], GetMaxLength method [Security],IEnumCERTVIEWCOLUMN interface, IEnumCERTVIEWCOLUMN interface [Security],GetMaxLength method, IEnumCERTVIEWCOLUMN.GetMaxLength, IEnumCERTVIEWCOLUMN::GetMaxLength, _certsrv_ienumcertviewcolumn_getmaxlength, certview/IEnumCERTVIEWCOLUMN::GetMaxLength, security.ienumcertviewcolumn_getmaxlength
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
 - IEnumCERTVIEWCOLUMN::GetMaxLength
 - certview/IEnumCERTVIEWCOLUMN::GetMaxLength
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
 - IEnumCERTVIEWCOLUMN.GetMaxLength
 - IEnumCERTVIEWCOLUMN.GetMaxLength
---

# IEnumCERTVIEWCOLUMN::GetMaxLength


## -description

The <b>GetMaxLength</b> method retrieves the maximum allowable length, in bytes, for the column data.

 If the column data's type is <b>PROPTYPE_STRING</b>, divide the number of bytes by <code>sizeof(WCHAR)</code> to determine the maximum number of <a href="/windows/desktop/SecGloss/u-gly">Unicode</a> characters.

## -parameters

### -param pMaxLength [out]

A pointer to a value of <b>LONG</b> type  that  contains the maximum allowable length for the column data. This function will fail if <i>pMaxLength</i> is <b>NULL</b>.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK and the <i>pMaxLength</i> is set to the  maximum allowable length for the column data.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the maximum allowable length, in bytes, for the column data.

## -remarks

This method is used to determine the maximum allowable data length for the column currently being referenced by the 
column-enumeration sequence.

If the column-enumeration sequence is not referencing a valid column, <b>GetMaxLength</b> will fail. Use one of the following methods to navigate through the enumeration:

<ul>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-reset">IEnumCERTVIEWCOLUMN::Reset</a>: Moves to the beginning of the enumeration sequence.</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-next">IEnumCERTVIEWCOLUMN::Next</a>: Moves to the next column in the enumeration sequence.</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-skip">IEnumCERTVIEWCOLUMN::Skip</a>: Skips a specified number of columns.</li>
</ul>
To determine whether the column data is indexed, call the <a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-isindexed">IEnumCERTVIEWCOLUMN::IsIndexed</a> method.


#### Examples


```cpp
// pEnumCol is previously instantiated IEnumCERTVIEWCOLUMN object
HRESULT  hr;
LONG     nLength;

// determine database length
hr = pEnumCol->GetMaxLength(&nLength);
if (S_OK == hr)
    printf("max length is %d\n", nLength);
```

## -see-also

<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewcolumn">IEnumCERTVIEWCOLUMN</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-isindexed">IEnumCERTVIEWCOLUMN::IsIndexed</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-next">IEnumCERTVIEWCOLUMN::Next</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-reset">IEnumCERTVIEWCOLUMN::Reset</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-skip">IEnumCERTVIEWCOLUMN::Skip</a>