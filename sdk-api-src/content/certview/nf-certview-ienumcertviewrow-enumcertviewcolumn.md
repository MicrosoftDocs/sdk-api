---
UID: NF:certview.IEnumCERTVIEWROW.EnumCertViewColumn
title: IEnumCERTVIEWROW::EnumCertViewColumn (certview.h)
description: Obtains an instance of a column-enumeration sequence for the current row of the row-enumeration sequence.
helpviewer_keywords: ["EnumCertViewColumn","EnumCertViewColumn method [Security]","EnumCertViewColumn method [Security]","IEnumCERTVIEWROW interface","IEnumCERTVIEWROW interface [Security]","EnumCertViewColumn method","IEnumCERTVIEWROW.EnumCertViewColumn","IEnumCERTVIEWROW::EnumCertViewColumn","_certsrv_ienumcertviewrow_enumcertviewcolumn","certview/IEnumCERTVIEWROW::EnumCertViewColumn","security.ienumcertviewrow_enumcertviewcolumn"]
old-location: security\ienumcertviewrow_enumcertviewcolumn.htm
tech.root: security
ms.assetid: 78fd2431-c4c7-4df9-856a-69665fa8c063
ms.date: 12/05/2018
ms.keywords: EnumCertViewColumn, EnumCertViewColumn method [Security], EnumCertViewColumn method [Security],IEnumCERTVIEWROW interface, IEnumCERTVIEWROW interface [Security],EnumCertViewColumn method, IEnumCERTVIEWROW.EnumCertViewColumn, IEnumCERTVIEWROW::EnumCertViewColumn, _certsrv_ienumcertviewrow_enumcertviewcolumn, certview/IEnumCERTVIEWROW::EnumCertViewColumn, security.ienumcertviewrow_enumcertviewcolumn
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
 - IEnumCERTVIEWROW::EnumCertViewColumn
 - certview/IEnumCERTVIEWROW::EnumCertViewColumn
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
 - IEnumCERTVIEWROW.EnumCertViewColumn
 - IEnumCERTVIEWROW.EnumCertViewColumn
---

# IEnumCERTVIEWROW::EnumCertViewColumn


## -description

The <b>EnumCertViewColumn</b> method obtains an instance of a column-enumeration sequence for the current row of the row-enumeration sequence.

## -parameters

### -param ppenum [out]

A pointer to a pointer of <a href="/windows/desktop/api/certview/nn-certview-ienumcertviewcolumn">IEnumCERTVIEWCOLUMN</a> type.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a column-enumeration sequence object.

## -remarks

The 
column-enumeration sequence obtained by this call can be used to enumerate the columns associated with the certificate in the current row. This enumeration can be accessed through the methods of the <a href="/windows/desktop/api/certview/nn-certview-ienumcertviewcolumn">IEnumCERTVIEWCOLUMN</a> interface.

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
// pEnumRow is previously instantiated pointer to IEnumCERTVIEWROW
HRESULT               hr;
LONG                  Index;
IEnumCERTVIEWCOLUMN * pEnumCol = NULL;
// obtain enumerator for columns
hr = pEnumRow->EnumCertViewColumn(&pEnumCol);
if ( FAILED( hr ))
{
    printf("Failed EnumCertViewColumn - %x\n", hr );
    goto error;
}
// enumerate each column
while (S_OK == pEnumCol->Next(&Index))
{
    // Use this column as needed.
}
error:

// Free resources.
if ( NULL != pEnumCol )
    pEnumCol->Release();
```

## -see-also

<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewcolumn">IEnumCERTVIEWCOLUMN</a>



<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewrow">IEnumCERTVIEWROW</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-next">IEnumCERTVIEWROW::Next</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-reset">IEnumCERTVIEWROW::Reset</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-skip">IEnumCERTVIEWROW::Skip</a>