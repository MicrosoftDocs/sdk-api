---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

