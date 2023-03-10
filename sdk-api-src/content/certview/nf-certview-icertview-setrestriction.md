---
UID: NF:certview.ICertView.SetRestriction
title: ICertView::SetRestriction (certview.h)
description: Sets the sorting and qualifying restrictions on a column.
helpviewer_keywords: ["CCertView object [Security]","SetRestriction method","CVR_SEEK_EQ","CVR_SEEK_GE","CVR_SEEK_GT","CVR_SEEK_LE","CVR_SEEK_LT","CVR_SORT_ASCEND","CVR_SORT_DESCEND","CVR_SORT_NONE","CV_COLUMN_LOG_DEFAULT","CV_COLUMN_LOG_FAILED_DEFAULT","CV_COLUMN_QUEUE_DEFAULT","ICertView interface [Security]","SetRestriction method","ICertView.SetRestriction","ICertView2 interface [Security]","SetRestriction method","ICertView2::SetRestriction","ICertView::SetRestriction","SetRestriction","SetRestriction method [Security]","SetRestriction method [Security]","CCertView object","SetRestriction method [Security]","ICertView interface","SetRestriction method [Security]","ICertView2 interface","certview/ICertView2::SetRestriction","certview/ICertView::SetRestriction","security.icertview2_setrestriction"]
old-location: security\icertview2_setrestriction.htm
tech.root: security
ms.assetid: a2dc8675-1d75-4c15-a9f7-971274ab044c
ms.date: 12/05/2018
ms.keywords: CCertView object [Security],SetRestriction method, CVR_SEEK_EQ, CVR_SEEK_GE, CVR_SEEK_GT, CVR_SEEK_LE, CVR_SEEK_LT, CVR_SORT_ASCEND, CVR_SORT_DESCEND, CVR_SORT_NONE, CV_COLUMN_LOG_DEFAULT, CV_COLUMN_LOG_FAILED_DEFAULT, CV_COLUMN_QUEUE_DEFAULT, ICertView interface [Security],SetRestriction method, ICertView.SetRestriction, ICertView2 interface [Security],SetRestriction method, ICertView2::SetRestriction, ICertView::SetRestriction, SetRestriction, SetRestriction method [Security], SetRestriction method [Security],CCertView object, SetRestriction method [Security],ICertView interface, SetRestriction method [Security],ICertView2 interface, certview/ICertView2::SetRestriction, certview/ICertView::SetRestriction, security.icertview2_setrestriction
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
 - ICertView::SetRestriction
 - certview/ICertView::SetRestriction
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
 - ICertView2.SetRestriction
 - ICertView.SetRestriction
 - CCertView.SetRestriction
---

# ICertView::SetRestriction


## -description

The <b>SetRestriction</b> method sets the sorting and qualifying restrictions on a column.

## -parameters

### -param ColumnIndex [in]

A valid column index number for the view or a predefined column specifier. If the <i>ColumnIndex</i> parameter is not negative, this value represents the zero-based index of the column that is receiving the restriction. 




If the <i>ColumnIndex</i> parameter is negative, all other parameters are ignored, and this parameter  must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CV_COLUMN_LOG_DEFAULT"></a><a id="cv_column_log_default"></a><dl>
<dt><b>CV_COLUMN_LOG_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Restricts view to requests that have been resolved. A request is resolved if it has resulted in an issued certificate or a failed request; revoked certificates are considered resolved.

</td>
</tr>
<tr>
<td width="40%"><a id="CV_COLUMN_LOG_FAILED_DEFAULT"></a><a id="cv_column_log_failed_default"></a><dl>
<dt><b>CV_COLUMN_LOG_FAILED_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Restricts view to requests that have failed.

</td>
</tr>
<tr>
<td width="40%"><a id="CV_COLUMN_QUEUE_DEFAULT"></a><a id="cv_column_queue_default"></a><dl>
<dt><b>CV_COLUMN_QUEUE_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Restricts view to requests that have not been resolved; if a request has resulted in either an issued certificate or a failed request, it will not be part of the view.

</td>
</tr>
</table>

### -param SeekOperator [in]

Specifies the logical operator of the data-query qualifier for the column. This parameter is used  with the <i>pvarValue</i> parameter to define the data-query qualifier.  This parameter must be set to one  of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CVR_SEEK_EQ"></a><a id="cvr_seek_eq"></a><dl>
<dt><b>CVR_SEEK_EQ</b></dt>
</dl>
</td>
<td width="60%">
Equal to

</td>
</tr>
<tr>
<td width="40%"><a id="CVR_SEEK_LE"></a><a id="cvr_seek_le"></a><dl>
<dt><b>CVR_SEEK_LE</b></dt>
</dl>
</td>
<td width="60%">
Less than or equal to

</td>
</tr>
<tr>
<td width="40%"><a id="CVR_SEEK_LT"></a><a id="cvr_seek_lt"></a><dl>
<dt><b>CVR_SEEK_LT</b></dt>
</dl>
</td>
<td width="60%">
Less than

</td>
</tr>
<tr>
<td width="40%"><a id="CVR_SEEK_GE"></a><a id="cvr_seek_ge"></a><dl>
<dt><b>CVR_SEEK_GE</b></dt>
</dl>
</td>
<td width="60%">
Greater than or equal to

</td>
</tr>
<tr>
<td width="40%"><a id="CVR_SEEK_GT"></a><a id="cvr_seek_gt"></a><dl>
<dt><b>CVR_SEEK_GT</b></dt>
</dl>
</td>
<td width="60%">
Greater than

</td>
</tr>
</table>

### -param SortOrder [in]

Specifies the sort order for the column. Indexed columns with zero or one restriction can include a sort order of  CVR_SORT_ASCEND or CVR_SORT_DESCEND. Nonindexed columns or columns with two or more restrictions  must use CVR_SORT_NONE.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CVR_SORT_ASCEND"></a><a id="cvr_sort_ascend"></a><dl>
<dt><b>CVR_SORT_ASCEND</b></dt>
</dl>
</td>
<td width="60%">
Ascending

</td>
</tr>
<tr>
<td width="40%"><a id="CVR_SORT_DESCEND"></a><a id="cvr_sort_descend"></a><dl>
<dt><b>CVR_SORT_DESCEND</b></dt>
</dl>
</td>
<td width="60%">
Descending

</td>
</tr>
<tr>
<td width="40%"><a id="CVR_SORT_NONE"></a><a id="cvr_sort_none"></a><dl>
<dt><b>CVR_SORT_NONE</b></dt>
</dl>
</td>
<td width="60%">
No sort order

</td>
</tr>
</table>

### -param pvarValue [in]

Specifies the data query qualifier applied to this column. This parameter, along with the <i>SeekOperator</i> parameter, determines which data is returned to the Certificate Services view.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The 
<a href="/windows/desktop/api/certview/nn-certview-icertview">ICertView</a> object maintains an array of restrictions, allowing each column to contain any number of restrictions. After the column restrictions are established, a call to the 
<a href="/windows/desktop/api/certview/nf-certview-icertview-openview">ICertView::OpenView</a> method will retrieve the data, with each column's restrictions used as part of the database query.

Before the <b>SetRestriction</b> method is called, it is necessary to establish a connection with the Certificate Service server by calling the 
<a href="/windows/desktop/api/certview/nf-certview-icertview-openconnection">ICertView::OpenConnection</a> method.


#### Examples


```cpp
    // This example restricts the data
    // to rows that have RequestIDs greater than five.
    // pCertView is a pointer to ICertView.
    HRESULT    hr;
    VARIANT    varRest;
    LONG       nIndex;
    BSTR       bstrCol = NULL;

    // Use one column in the result set.
    hr = pCertView->SetResultColumnCount(1);
    if (FAILED(hr))
    {
        printf("Failed SetResultColumnCount - %x\n", hr);
        goto error;
    }
    // Determine the column index for RequestID column.
    bstrCol = SysAllocString(TEXT("RequestID"));
    hr = pCertView->GetColumnIndex(FALSE, bstrCol, &nIndex);
    if (FAILED(hr))
    {
        printf("Failed GetColumnIndex - %x\n", hr);
        goto error;
    }
    // Place this column into the result set.
    pCertView->SetResultColumn(nIndex);
    // Set a restriction on this column.
    VariantInit(&varRest);
    varRest.vt = VT_I4;
    varRest.lVal = 5;
    // Restrict view to requests with ID greater than 5.
    hr = pCertView->SetRestriction(nIndex,
                                   CVR_SEEK_GT,
                                   CVR_SORT_NONE,
                                   &varRest);
    if (S_OK != hr)
        printf("Failed ICertView::SetRestriction - %x\n", hr);
    else
	{
        // Call OpenView, process rows, release resources, and so on.
        // ...
	}
error:
    // Done processing, clear resources.
    VariantClear(&varRest);
    if (NULL != bstrCol)
        SysFreeString(bstrCol);
```

## -see-also

<a href="/windows/desktop/api/certview/nn-certview-icertview">ICertView</a>



<a href="/windows/desktop/api/certview/nn-certview-icertview2">ICertView2</a>



<a href="/windows/desktop/api/certview/nf-certview-icertview-openconnection">ICertView::OpenConnection</a>



<a href="/windows/desktop/api/certview/nf-certview-icertview-openview">ICertView::OpenView</a>



<a href="/windows/desktop/api/certview/nf-certview-icertview-setresultcolumn">ICertView::SetResultColumn</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-isindexed">IEnumCertViewColumn::IsIndexed</a>