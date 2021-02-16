---
UID: NF:certview.ICertView.SetResultColumn
title: ICertView::SetResultColumn (certview.h)
description: Specifies a column for the result set of a customized view of the Certificate Services database.
helpviewer_keywords: ["CCertView object [Security]","SetResultColumn method","ICertView interface [Security]","SetResultColumn method","ICertView.SetResultColumn","ICertView2 interface [Security]","SetResultColumn method","ICertView2::SetResultColumn","ICertView::SetResultColumn","SetResultColumn","SetResultColumn method [Security]","SetResultColumn method [Security]","CCertView object","SetResultColumn method [Security]","ICertView interface","SetResultColumn method [Security]","ICertView2 interface","certview/ICertView2::SetResultColumn","certview/ICertView::SetResultColumn","security.icertview2_setresultcolumn"]
old-location: security\icertview2_setresultcolumn.htm
tech.root: security
ms.assetid: c13bdc3a-e623-49df-bba0-34c4c178dc3b
ms.date: 12/05/2018
ms.keywords: CCertView object [Security],SetResultColumn method, ICertView interface [Security],SetResultColumn method, ICertView.SetResultColumn, ICertView2 interface [Security],SetResultColumn method, ICertView2::SetResultColumn, ICertView::SetResultColumn, SetResultColumn, SetResultColumn method [Security], SetResultColumn method [Security],CCertView object, SetResultColumn method [Security],ICertView interface, SetResultColumn method [Security],ICertView2 interface, certview/ICertView2::SetResultColumn, certview/ICertView::SetResultColumn, security.icertview2_setresultcolumn
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
 - ICertView::SetResultColumn
 - certview/ICertView::SetResultColumn
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
 - ICertView2.SetResultColumn
 - ICertView.SetResultColumn
 - CCertView.SetResultColumn
---

# ICertView::SetResultColumn


## -description

The <b>SetResultColumn</b> method specifies a column for the result set of a customized view of the Certificate Services database.

## -parameters

### -param ColumnIndex [in]

A zero-based index of a column to include in the result set.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Before calling the <b>SetResultColumn</b> method, the <a href="/windows/desktop/api/certview/nf-certview-icertview-setresultcolumncount">SetResultColumnCount</a> method must be called to specify how many columns will be in the result set. Calls to the <b>SetResultColumn</b> method will fail under the following conditions:

<ul>
<li>The number of columns has not been specified.</li>
<li><b>SetResultColumn</b> is called more times than the number of columns specified by the call to <a href="/windows/desktop/api/certview/nf-certview-icertview-setresultcolumncount">SetResultColumnCount</a>.</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-icertview-setresultcolumncount">SetResultColumnCount</a> specified a predefined set of columns.  This method specifies a predefined set of columns when its <i>cResultColumnCount</i> parameter is one of the following values:<ul>
<li>CV_COLUMN_LOG_DEFAULT</li>
<li>CV_COLUMN_LOG_FAILED_DEFAULT</li>
<li>CV_COLUMN_QUEUE_DEFAULT</li>
</ul>
</li>
</ul>
After a column is specified, an optional call to the 
<a href="/windows/desktop/api/certview/nf-certview-icertview-setrestriction">SetRestriction</a> method can be used to specify sorting and qualifying restrictions for the column.

The <b>SetResultColumn</b> method must be called for each column that is needed in the result set. On successful completion of these calls, the columns specified in each call will be included in the result set when the <a href="/windows/desktop/api/certview/nf-certview-icertview-openview">OpenView</a> method is called.


#### Examples


```cpp
    HRESULT    hr;
    LONG       nCount;
    LONG       i;

    // Determine the number of columns in the entire database.
    // pCertView is a pointer to ICertView.
    hr = pCertView->GetColumnCount(FALSE, &nCount);
    if (FAILED(hr))
    {
        printf("Failed GetColumnCount - %x\n", hr);
        goto error;
    }
    hr = pCertView->SetResultColumnCount( nCount );
    if (FAILED(hr))
    {
        printf("Failed SetResultColumnCount - %x\n", hr);
        goto error;
    }
    // Place each column in the view.
    for (i = 0; i < nCount; i++)
    {
        hr = pCertView->SetResultColumn(i);
        if (FAILED(hr))
        {
            printf("Failed SetResultColumn (%d) - %x\n", i, hr );
            goto error;
        }
    }
    // Call ICertView::OpenView, and so on.
    // ...

error:
	{
		 // Clean up resources, and so on.
	}
```

## -see-also

<a href="/windows/desktop/api/certview/nn-certview-icertview">ICertView</a>



<a href="/windows/desktop/api/certview/nn-certview-icertview2">ICertView2</a>



<a href="/windows/desktop/api/certview/nf-certview-icertview-openview">ICertView::OpenView</a>



<a href="/windows/desktop/api/certview/nf-certview-icertview-setrestriction">ICertView::SetRestriction</a>



<a href="/windows/desktop/api/certview/nf-certview-icertview-setresultcolumncount">ICertView::SetResultColumnCount</a>