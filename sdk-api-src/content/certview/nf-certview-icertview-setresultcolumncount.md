---
UID: NF:certview.ICertView.SetResultColumnCount
title: ICertView::SetResultColumnCount
author: windows-sdk-content
description: Specifies the maximum number of columns for the result set of a customized view of the Certificate Services database.
old-location: security\icertview2_setresultcolumncount.htm
tech.root: seccrypto
ms.assetid: f98b2f45-be9f-47ba-9c6b-63a2912288ac
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CCertView object [Security],SetResultColumnCount method, CV_COLUMN_LOG_DEFAULT, CV_COLUMN_LOG_FAILED_DEFAULT, CV_COLUMN_QUEUE_DEFAULT, ICertView interface [Security],SetResultColumnCount method, ICertView.SetResultColumnCount, ICertView2 interface [Security],SetResultColumnCount method, ICertView2::SetResultColumnCount, ICertView::SetResultColumnCount, SetResultColumnCount, SetResultColumnCount method [Security], SetResultColumnCount method [Security],CCertView object, SetResultColumnCount method [Security],ICertView interface, SetResultColumnCount method [Security],ICertView2 interface, certview/ICertView2::SetResultColumnCount, certview/ICertView::SetResultColumnCount, security.icertview2_setresultcolumncount
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
 - ICertView2.SetResultColumnCount
 - ICertView.SetResultColumnCount
 - CCertView.SetResultColumnCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertView::SetResultColumnCount


## -description


The <b>SetResultColumnCount</b> method specifies the maximum  number of columns for the result set of a customized view of the Certificate Services database.


## -parameters




### -param cResultColumn [in]

Specifies the maximum number of columns in the result set. This parameter can be set to a positive number, or to zero if you are only interested in counting the rows of the Certificate Services database, or to one of the following constants.

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
The number of columns in the result set will be the number of columns in the Certificate Services's default result set for requests that have been resolved. A request is resolved if it has resulted in an issued certificate or a failed request; revoked certificates are considered resolved.

</td>
</tr>
<tr>
<td width="40%"><a id="CV_COLUMN_LOG_FAILED_DEFAULT"></a><a id="cv_column_log_failed_default"></a><dl>
<dt><b>CV_COLUMN_LOG_FAILED_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The number of columns in the result set will be the number of columns in the Certificate Services's default result set for requests that have failed.

</td>
</tr>
<tr>
<td width="40%"><a id="CV_COLUMN_QUEUE_DEFAULT"></a><a id="cv_column_queue_default"></a><dl>
<dt><b>CV_COLUMN_QUEUE_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The number of columns in the result set will be the number of columns in the Certificate Services's default result set for requests that have not been resolved.

</td>
</tr>
</table>
 


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -remarks



Before calling the <b>SetResultColumnCount</b> method, it is necessary to establish a connection with a Certificate Services server by calling the 
<a href="https://msdn.microsoft.com/en-us/library/Aa385432(v=VS.85).aspx">OpenConnection</a> method first. After the connection is established, this method can be called once, and only once, to specify the maximum number of columns in the result set.

If the <i>cResultColumn</i> parameter is set to a positive number (not one of the predefined constants), the 
<a href="https://msdn.microsoft.com/en-us/library/Aa385442(v=VS.85).aspx">SetResultColumn</a> method must be called to specify which  columns to include in the  result set. Note that <b>SetResultColumn</b> fails if it is called more than the number of columns specified by <b>SetResultColumnCount</b>.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT    hr;
// Specify the result set for logged requests.
// pCertView is pointer to ICertView (which has an Open Connection)
hr = pCertView-&gt;SetResultColumnCount(CV_COLUMN_LOG_DEFAULT);
if (S_OK != hr)
    printf("Failed ICertView::SetResultColumnCount - %x\n", hr);
else
{
    // Retrieve data rows by means of ICertView::OpenView.
    // ...
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa385414(v=VS.85).aspx">ICertView</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385417(v=VS.85).aspx">ICertView2</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385432(v=VS.85).aspx">ICertView::OpenConnection</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385439(v=VS.85).aspx">ICertView::SetRestriction</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385442(v=VS.85).aspx">ICertView::SetResultColumn</a>
 

 

