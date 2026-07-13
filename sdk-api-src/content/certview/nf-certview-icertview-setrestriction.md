---
UID: NF:certview.ICertView.SetRestriction
title: ICertView::SetRestriction (certview.h)
description: Sets the sorting and qualifying restrictions on a column.
helpviewer_keywords: ["CCertView object [Security]","SetRestriction method","CVR_SEEK_EQ","CVR_SEEK_GE","CVR_SEEK_GT","CVR_SEEK_LE","CVR_SEEK_LT","CVR_SORT_ASCEND","CVR_SORT_DESCEND","CVR_SORT_NONE","CV_COLUMN_LOG_DEFAULT","CV_COLUMN_LOG_FAILED_DEFAULT","CV_COLUMN_QUEUE_DEFAULT","ICertView interface [Security]","SetRestriction method","ICertView.SetRestriction","ICertView2 interface [Security]","SetRestriction method","ICertView2::SetRestriction","ICertView::SetRestriction","SetRestriction","SetRestriction method [Security]","SetRestriction method [Security]","CCertView object","SetRestriction method [Security]","ICertView interface","SetRestriction method [Security]","ICertView2 interface","certview/ICertView2::SetRestriction","certview/ICertView::SetRestriction","security.icertview2_setrestriction"]
old-location: security\icertview2_setrestriction.htm
tech.root: security
ms.assetid: a2dc8675-1d75-4c15-a9f7-971274ab044c
ms.date: 01/08/2025
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

The **SetRestriction** method sets the sorting and qualifying restrictions on a column.

## -parameters

### -param ColumnIndex [in]

A valid column index number for the view or a predefined column specifier. If the *ColumnIndex* parameter is not negative, this value represents the zero-based index of the column that is receiving the restriction.

If the *ColumnIndex* parameter is negative, all other parameters are ignored, and this parameter must be one of the following values:

| Value | Meaning |
|-------|---------|
| **CV_COLUMN_QUEUE_DEFAULT**<br/>`-1` | Restricts view to requests that have not been resolved; if a request has resulted in either an issued certificate or a failed request, it will not be part of the view. |
| **CV_COLUMN_LOG_DEFAULT**<br/>`-2` | Restricts view to requests that have been resolved. A request is resolved if it has resulted in an issued certificate or a failed request; revoked certificates are considered resolved. |
| **CV_COLUMN_LOG_FAILED_DEFAULT**<br/>`-3` | Restricts view to requests that have failed. |

### -param SeekOperator [in]

Specifies the logical operator of the data-query qualifier for the column. This parameter is used  with the *pvarValue* parameter to define the data-query qualifier.

This parameter must be set to one  of the following values:

| Value | Meaning |
|-------|---------|
| **CVR_SEEK_EQ**<br/>`0x1`  | Equal to |
| **CVR_SEEK_LT**<br/>`0x2`  | Less than |
| **CVR_SEEK_LE**<br/>`0x4`  | Less than or equal to |
| **CVR_SEEK_GE**<br/>`0x8`  | Greater than or equal to |
| **CVR_SEEK_GT**<br/>`0x10` | Greater than |

### -param SortOrder [in]

Specifies the sort order for the column. Indexed columns with zero or one restriction can include a sort order of **CVR_SORT_ASCEND** or **CVR_SORT_DESCEND**. Non-indexed columns or columns with two or more restrictions must use **CVR_SORT_NONE**.

| Value | Meaning |
|-------|---------|
| **CVR_SORT_NONE**<br/>`0`      | No sort order |
| **CVR_SORT_ASCEND**<br/>`0x1`  | Ascending |
| **CVR_SORT_DESCEND**<br/>`0x2` | Descending |

### -param pvarValue [in]

Specifies the data query qualifier applied to this column. This parameter, along with the *SeekOperator* parameter, determines which data is returned to the Certificate Services view.

## -returns

If the method succeeds, the method returns **S_OK**.

If the method fails, it returns an **HRESULT** value that indicates the error. For a list of common error codes, see [Common HRESULT Values](/windows/win32/SecCrypto/common-hresult-values).

## -remarks

The [ICertView](nn-certview-icertview.md) object maintains an array of restrictions, allowing each column to contain any number of restrictions. After the column restrictions are established, a call to the [ICertView::OpenView](nf-certview-icertview-openview.md) method will retrieve the data, with each column's restrictions used as part of the database query.

Before the **SetRestriction** method is called, it is necessary to establish a connection with the Certificate Service server by calling the[ICertView::OpenConnection](nf-certview-icertview-openconnection.md) method.

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

[ICertView](nn-certview-icertview.md)

[ICertView2](nn-certview-icertview2.md)

[ICertView::OpenConnection](nf-certview-icertview-openconnection.md)

[ICertView::OpenView](nf-certview-icertview-openview.md)

[ICertView::SetResultColumn](nf-certview-icertview-setresultcolumn.md)

[IEnumCertViewColumn::IsIndexed](nf-certview-ienumcertviewcolumn-isindexed.md)
