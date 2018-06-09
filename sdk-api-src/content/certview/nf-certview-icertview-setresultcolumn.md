---
UID: NF:certview.ICertView.SetResultColumn
title: ICertView::SetResultColumn
author: windows-sdk-content
description: Specifies a column for the result set of a customized view of the Certificate Services database.
old-location: security\icertview2_setresultcolumn.htm
old-project: SecCrypto
ms.assetid: c13bdc3a-e623-49df-bba0-34c4c178dc3b
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: CCertView object [Security],SetResultColumn method, ICertView interface [Security],SetResultColumn method, ICertView.SetResultColumn, ICertView2 interface [Security],SetResultColumn method, ICertView2::SetResultColumn, ICertView::SetResultColumn, SetResultColumn, SetResultColumn method [Security], SetResultColumn method [Security],CCertView object, SetResultColumn method [Security],ICertView interface, SetResultColumn method [Security],ICertView2 interface, certview/ICertView2::SetResultColumn, certview/ICertView::SetResultColumn, security.icertview2_setresultcolumn
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ENUM_CATYPES
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
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
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

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Before calling the <b>SetResultColumn</b> method, the <a href="https://msdn.microsoft.com/f98b2f45-be9f-47ba-9c6b-63a2912288ac">SetResultColumnCount</a> method must be called to specify how many columns will be in the result set. Calls to the <b>SetResultColumn</b> method will fail under the following conditions:

<ul>
<li>The number of columns has not been specified.</li>
<li><b>SetResultColumn</b> is called more times than the number of columns specified by the call to <a href="https://msdn.microsoft.com/f98b2f45-be9f-47ba-9c6b-63a2912288ac">SetResultColumnCount</a>.</li>
<li>
<a href="https://msdn.microsoft.com/f98b2f45-be9f-47ba-9c6b-63a2912288ac">SetResultColumnCount</a> specified a predefined set of columns.  This method specifies a predefined set of columns when its <i>cResultColumnCount</i> parameter is one of the following values:<ul>
<li>CV_COLUMN_LOG_DEFAULT</li>
<li>CV_COLUMN_LOG_FAILED_DEFAULT</li>
<li>CV_COLUMN_QUEUE_DEFAULT</li>
</ul>
</li>
</ul>
After a column is specified, an optional call to the 
<a href="https://msdn.microsoft.com/a2dc8675-1d75-4c15-a9f7-971274ab044c">SetRestriction</a> method can be used to specify sorting and qualifying restrictions for the column.

The <b>SetResultColumn</b> method must be called for each column that is needed in the result set. On successful completion of these calls, the columns specified in each call will be included in the result set when the <a href="https://msdn.microsoft.com/d68a5463-f711-4737-b0ad-889f7e4855d5">OpenView</a> method is called.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    HRESULT    hr;
    LONG       nCount;
    LONG       i;

    // Determine the number of columns in the entire database.
    // pCertView is a pointer to ICertView.
    hr = pCertView-&gt;GetColumnCount(FALSE, &amp;nCount);
    if (FAILED(hr))
    {
        printf("Failed GetColumnCount - %x\n", hr);
        goto error;
    }
    hr = pCertView-&gt;SetResultColumnCount( nCount );
    if (FAILED(hr))
    {
        printf("Failed SetResultColumnCount - %x\n", hr);
        goto error;
    }
    // Place each column in the view.
    for (i = 0; i &lt; nCount; i++)
    {
        hr = pCertView-&gt;SetResultColumn(i);
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
	}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/0b6660ee-458f-457f-8a38-0d950aee2710">ICertView</a>



<a href="https://msdn.microsoft.com/c29f1db3-0cdf-463e-a202-47fbba8e1c81">ICertView2</a>



<a href="https://msdn.microsoft.com/d68a5463-f711-4737-b0ad-889f7e4855d5">ICertView::OpenView</a>



<a href="https://msdn.microsoft.com/a2dc8675-1d75-4c15-a9f7-971274ab044c">ICertView::SetRestriction</a>



<a href="https://msdn.microsoft.com/f98b2f45-be9f-47ba-9c6b-63a2912288ac">ICertView::SetResultColumnCount</a>
 

 

