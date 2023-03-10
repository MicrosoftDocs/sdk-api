---
UID: NF:certview.IEnumCERTVIEWROW.Next
title: IEnumCERTVIEWROW::Next (certview.h)
description: Moves to the next row in the row-enumeration sequence.
helpviewer_keywords: ["IEnumCERTVIEWROW interface [Security]","Next method","IEnumCERTVIEWROW.Next","IEnumCERTVIEWROW::Next","Next","Next method [Security]","Next method [Security]","IEnumCERTVIEWROW interface","_certsrv_ienumcertviewrow_next","certview/IEnumCERTVIEWROW::Next","security.ienumcertviewrow_next"]
old-location: security\ienumcertviewrow_next.htm
tech.root: security
ms.assetid: 6e471ee9-4b69-468c-a724-e43bd93419d9
ms.date: 12/05/2018
ms.keywords: IEnumCERTVIEWROW interface [Security],Next method, IEnumCERTVIEWROW.Next, IEnumCERTVIEWROW::Next, Next, Next method [Security], Next method [Security],IEnumCERTVIEWROW interface, _certsrv_ienumcertviewrow_next, certview/IEnumCERTVIEWROW::Next, security.ienumcertviewrow_next
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
 - IEnumCERTVIEWROW::Next
 - certview/IEnumCERTVIEWROW::Next
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
 - IEnumCERTVIEWROW.Next
 - IEnumCERTVIEWROW.Next
---

# IEnumCERTVIEWROW::Next


## -description

The <b>Next</b> method moves to the next row in the row-enumeration sequence.

## -parameters

### -param pIndex [out]

A pointer to a variable that contains the index value of the next row being  referenced. If there are no more rows to enumerate, this variable will be set to –1. This method fails if <i>pIndex</i> is <b>NULL</b>.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK and the next row is now being referenced by the row-enumeration sequence. If there are no more rows to enumerate, S_FALSE is returned, and <i>pIndex</i> is set to a value of –1.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the index value of the  row that is now being referenced by the row-enumeration sequence. If there are no more rows to enumerate, the return value is –1.

## -remarks

Upon successful completion of this method, the 
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
Looping through all the  rows in the enumeration sequence can be resource-intensive to compute, depending of the query involved and the  size of the sequence.


#### Examples


```cpp
// pEnumRow is previously instantiated pointer to IEnumCERTVIEWROW.
LONG  Index;
LONG  nCount;

// Ensure enumerator is at first row.
if (FAILED(pEnumRow->Reset()))
    printf("Failed to Reset\n");
else
{
    nCount = 0;
    // Count the database records by enumerating the rows.
    while (S_OK == pEnumRow->Next(&Index))
        nCount++;
    // Display number of records.
    printf("Number of records is %d\n", nCount);
}
```

## -see-also

<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewattribute">IEnumCERTVIEWATTRIBUTE</a>



<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewcolumn">IEnumCERTVIEWCOLUMN</a>



<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewextension">IEnumCERTVIEWEXTENSION</a>



<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewrow">IEnumCERTVIEWROW</a>