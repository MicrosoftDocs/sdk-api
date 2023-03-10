---
UID: NF:certview.IEnumCERTVIEWROW.GetMaxIndex
title: IEnumCERTVIEWROW::GetMaxIndex (certview.h)
description: Retrieves the maximum valid index value after all the rows in the row-enumeration sequence have been referenced.
helpviewer_keywords: ["GetMaxIndex","GetMaxIndex method [Security]","GetMaxIndex method [Security]","IEnumCERTVIEWROW interface","IEnumCERTVIEWROW interface [Security]","GetMaxIndex method","IEnumCERTVIEWROW.GetMaxIndex","IEnumCERTVIEWROW::GetMaxIndex","certview/IEnumCERTVIEWROW::GetMaxIndex","security.ienumcertviewrow_getmaxindex","security.ienumcertviewrow_getmaxtindex"]
old-location: security\ienumcertviewrow_getmaxindex.htm
tech.root: SecCrypto
ms.assetid: 65ba80db-b7ee-46fa-b044-eab554720ce9
ms.date: 12/05/2018
ms.keywords: GetMaxIndex, GetMaxIndex method [Security], GetMaxIndex method [Security],IEnumCERTVIEWROW interface, IEnumCERTVIEWROW interface [Security],GetMaxIndex method, IEnumCERTVIEWROW.GetMaxIndex, IEnumCERTVIEWROW::GetMaxIndex, certview/IEnumCERTVIEWROW::GetMaxIndex, security.ienumcertviewrow_getmaxindex, security.ienumcertviewrow_getmaxtindex
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
 - IEnumCERTVIEWROW::GetMaxIndex
 - certview/IEnumCERTVIEWROW::GetMaxIndex
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
 - IEnumCERTVIEWROW.GetMaxIndex
 - IEnumCERTVIEWROW.GetMaxIndex
---

# IEnumCERTVIEWROW::GetMaxIndex


## -description

The <b>GetMaxIndex</b> method retrieves the maximum valid index value after all the rows in the row-enumeration sequence have been referenced.

## -parameters

### -param pIndex [out]

A pointer to a <b>LONG</b> variable that contains the maximum index value for the row-enumeration sequence. This method fails if <i>pIndex</i> is <b>NULL</b>.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK and <i>pIndex</i> is set to the maximum index value for the row-enumeration sequence.

If traversal to the last row has not occurred, this method fails with a return value of E_UNEXPECTED.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the maximum index value for the row-enumeration sequence. This method fails if traversal to the last row has not occurred.

## -remarks

Successful completion of this method is dependent on reaching the last row of the enumeration sequence. The maximum row index can be useful to size a scroll bar or display window, but it can also be resource-intensive to compute because it requires evaluating the entire query. For some queries, column data for each row must be examined to determine whether it is included in the view. After the user has paged through all of the data or explicitly requested to proceed to the end, the maximum row index is preserved.

To navigate through the row-enumeration sequence, call the following methods.

<table>
<tr>
<th>Method</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-reset">IEnumCERTVIEWROW::Reset</a>
</td>
<td>Moves to the beginning of the enumeration sequence.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-next">IEnumCERTVIEWROW::Next</a>
</td>
<td>Moves to the next row in the enumeration sequence.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-skip">IEnumCERTVIEWROW::Skip</a>
</td>
<td>Skips a specified number of rows.</td>
</tr>
</table>
 


#### Examples


```cpp
#include <windows.h>
#include <stdio.h>
#include <Certview.h>

long nMax;

//  Determine the maximum row index.
hr = pRow->GetMaxIndex(&nMax);
if (FAILED(hr))
    printf("Failed GetMaxIndex [%x]\n", hr);
else
    printf("Max index is: %d\n", nMax);

```

## -see-also

<b>IEnumCERTVIEWROW</b>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-next">IEnumCERTVIEWROW::Next</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-reset">IEnumCERTVIEWROW::Reset</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-skip">IEnumCERTVIEWROW::Skip</a>