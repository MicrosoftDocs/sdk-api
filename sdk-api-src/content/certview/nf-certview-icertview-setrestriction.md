---
UID: NF:certview.ICertView.SetRestriction
title: ICertView::SetRestriction
author: windows-sdk-content
description: Sets the sorting and qualifying restrictions on a column.
old-location: security\icertview2_setrestriction.htm
tech.root: seccrypto
ms.assetid: a2dc8675-1d75-4c15-a9f7-971274ab044c
ms.author: windowssdkdev
ms.date: 12/04/2018
ms.keywords: CCertView object [Security],SetRestriction method, CVR_SEEK_EQ, CVR_SEEK_GE, CVR_SEEK_GT, CVR_SEEK_LE, CVR_SEEK_LT, CVR_SORT_ASCEND, CVR_SORT_DESCEND, CVR_SORT_NONE, CV_COLUMN_LOG_DEFAULT, CV_COLUMN_LOG_FAILED_DEFAULT, CV_COLUMN_QUEUE_DEFAULT, ICertView interface [Security],SetRestriction method, ICertView.SetRestriction, ICertView2 interface [Security],SetRestriction method, ICertView2::SetRestriction, ICertView::SetRestriction, SetRestriction, SetRestriction method [Security], SetRestriction method [Security],CCertView object, SetRestriction method [Security],ICertView interface, SetRestriction method [Security],ICertView2 interface, certview/ICertView2::SetRestriction, certview/ICertView::SetRestriction, security.icertview2_setrestriction
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The 
<a href="https://msdn.microsoft.com/0b6660ee-458f-457f-8a38-0d950aee2710">ICertView</a> object maintains an array of restrictions, allowing each column to contain any number of restrictions. After the column restrictions are established, a call to the 
<a href="https://msdn.microsoft.com/d68a5463-f711-4737-b0ad-889f7e4855d5">ICertView::OpenView</a> method will retrieve the data, with each column's restrictions used as part of the database query.

Before the <b>SetRestriction</b> method is called, it is necessary to establish a connection with the Certificate Service server by calling the 
<a href="https://msdn.microsoft.com/576af4d1-88c9-40e3-9438-9fefd483be7a">ICertView::OpenConnection</a> method.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    // This example restricts the data
    // to rows that have RequestIDs greater than five.
    // pCertView is a pointer to ICertView.
    HRESULT    hr;
    VARIANT    varRest;
    LONG       nIndex;
    BSTR       bstrCol = NULL;

    // Use one column in the result set.
    hr = pCertView-&gt;SetResultColumnCount(1);
    if (FAILED(hr))
    {
        printf("Failed SetResultColumnCount - %x\n", hr);
        goto error;
    }
    // Determine the column index for RequestID column.
    bstrCol = SysAllocString(TEXT("RequestID"));
    hr = pCertView-&gt;GetColumnIndex(FALSE, bstrCol, &amp;nIndex);
    if (FAILED(hr))
    {
        printf("Failed GetColumnIndex - %x\n", hr);
        goto error;
    }
    // Place this column into the result set.
    pCertView-&gt;SetResultColumn(nIndex);
    // Set a restriction on this column.
    VariantInit(&amp;varRest);
    varRest.vt = VT_I4;
    varRest.lVal = 5;
    // Restrict view to requests with ID greater than 5.
    hr = pCertView-&gt;SetRestriction(nIndex,
                                   CVR_SEEK_GT,
                                   CVR_SORT_NONE,
                                   &amp;varRest);
    if (S_OK != hr)
        printf("Failed ICertView::SetRestriction - %x\n", hr);
    else
	{
        // Call OpenView, process rows, release resources, and so on.
        // ...
	}
error:
    // Done processing, clear resources.
    VariantClear(&amp;varRest);
    if (NULL != bstrCol)
        SysFreeString(bstrCol);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/0b6660ee-458f-457f-8a38-0d950aee2710">ICertView</a>



<a href="https://msdn.microsoft.com/c29f1db3-0cdf-463e-a202-47fbba8e1c81">ICertView2</a>



<a href="https://msdn.microsoft.com/576af4d1-88c9-40e3-9438-9fefd483be7a">ICertView::OpenConnection</a>



<a href="https://msdn.microsoft.com/d68a5463-f711-4737-b0ad-889f7e4855d5">ICertView::OpenView</a>



<a href="https://msdn.microsoft.com/c13bdc3a-e623-49df-bba0-34c4c178dc3b">ICertView::SetResultColumn</a>



<a href="https://msdn.microsoft.com/7373c0c3-3a1d-4a32-90e6-0f0575a0b61b">IEnumCertViewColumn::IsIndexed</a>
 

 

