---
UID: NF:certview.ICertView.GetColumnIndex
title: ICertView::GetColumnIndex (certview.h)
description: Retrieves the zero-based index of a column.
helpviewer_keywords: ["CCertView object [Security]","GetColumnIndex method","CVRC_COLUMN_MASK","CVRC_COLUMN_RESULT","CVRC_COLUMN_SCHEMA","CVRC_COLUMN_VALUE","GetColumnIndex","GetColumnIndex method [Security]","GetColumnIndex method [Security]","CCertView object","GetColumnIndex method [Security]","ICertView interface","GetColumnIndex method [Security]","ICertView2 interface","ICertView interface [Security]","GetColumnIndex method","ICertView.GetColumnIndex","ICertView2 interface [Security]","GetColumnIndex method","ICertView2::GetColumnIndex","ICertView::GetColumnIndex","certview/ICertView2::GetColumnIndex","certview/ICertView::GetColumnIndex","security.icertview2_getcolumnindex"]
old-location: security\icertview2_getcolumnindex.htm
tech.root: SecCrypto
ms.assetid: 3d869db9-b4df-4fcd-85e7-19fe773b4262
ms.date: 12/05/2018
ms.keywords: CCertView object [Security],GetColumnIndex method, CVRC_COLUMN_MASK, CVRC_COLUMN_RESULT, CVRC_COLUMN_SCHEMA, CVRC_COLUMN_VALUE, GetColumnIndex, GetColumnIndex method [Security], GetColumnIndex method [Security],CCertView object, GetColumnIndex method [Security],ICertView interface, GetColumnIndex method [Security],ICertView2 interface, ICertView interface [Security],GetColumnIndex method, ICertView.GetColumnIndex, ICertView2 interface [Security],GetColumnIndex method, ICertView2::GetColumnIndex, ICertView::GetColumnIndex, certview/ICertView2::GetColumnIndex, certview/ICertView::GetColumnIndex, security.icertview2_getcolumnindex
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
 - ICertView::GetColumnIndex
 - certview/ICertView::GetColumnIndex
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
 - ICertView2.GetColumnIndex
 - ICertView.GetColumnIndex
 - CCertView.GetColumnIndex
---

# ICertView::GetColumnIndex


## -description

The <b>GetColumnIndex</b> method retrieves the zero-based index of a column.

## -parameters

### -param fResultColumn [in]

Specifies the  column. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CVRC_COLUMN_SCHEMA"></a><a id="cvrc_column_schema"></a><dl>
<dt><b>CVRC_COLUMN_SCHEMA</b></dt>
</dl>
</td>
<td width="60%">
Schema column information.

</td>
</tr>
<tr>
<td width="40%"><a id="CVRC_COLUMN_RESULT"></a><a id="cvrc_column_result"></a><dl>
<dt><b>CVRC_COLUMN_RESULT</b></dt>
</dl>
</td>
<td width="60%">
Result column information.

</td>
</tr>
<tr>
<td width="40%"><a id="CVRC_COLUMN_VALUE"></a><a id="cvrc_column_value"></a><dl>
<dt><b>CVRC_COLUMN_VALUE</b></dt>
</dl>
</td>
<td width="60%">
Value column information.

</td>
</tr>
<tr>
<td width="40%"><a id="CVRC_COLUMN_MASK"></a><a id="cvrc_column_mask"></a><dl>
<dt><b>CVRC_COLUMN_MASK</b></dt>
</dl>
</td>
<td width="60%">
Column information mask.

</td>
</tr>
</table>

### -param strColumnName [in]

A string that contains the nonlocalized name of a column in the view.

### -param pColumnIndex [out, retval]

The address of a variable that will contain the index of the column specified in the <i>strColumnName</i> parameter. This method fails if <i>pColumnIndex</i> is <b>NULL</b>.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the zero-based index of the column.

## -remarks

This method is used to determine the index of the column specified by the <i>strColumnName</i> parameter. The column indices are zero-based (the first column is index zero).

## -see-also

<a href="/windows/desktop/api/certview/nn-certview-icertview">ICertView</a>



<a href="/windows/desktop/api/certview/nn-certview-icertview2">ICertView2</a>



<a href="/windows/desktop/api/certview/nf-certview-icertview-setrestriction">ICertView::SetRestriction</a>