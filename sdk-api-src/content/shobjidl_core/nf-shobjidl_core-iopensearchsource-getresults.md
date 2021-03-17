---
UID: NF:shobjidl_core.IOpenSearchSource.GetResults
title: IOpenSearchSource::GetResults (shobjidl_core.h)
description: Returns search results, from an OpenSearch data source, formatted in RSS or Atom format.
helpviewer_keywords: ["GetResults","GetResults method [Windows Shell]","GetResults method [Windows Shell]","IOpenSearchSource interface","IOpenSearchSource interface [Windows Shell]","GetResults method","IOpenSearchSource.GetResults","IOpenSearchSource::GetResults","_shell_IOpenSearchSource_GetResults","shell.IOpenSearchSource_GetResults","shobjidl_core/IOpenSearchSource::GetResults"]
old-location: shell\IOpenSearchSource_GetResults.htm
tech.root: shell
ms.assetid: 4fc16c04-cfb6-4f50-8325-bd3fc0b8f557
ms.date: 12/05/2018
ms.keywords: GetResults, GetResults method [Windows Shell], GetResults method [Windows Shell],IOpenSearchSource interface, IOpenSearchSource interface [Windows Shell],GetResults method, IOpenSearchSource.GetResults, IOpenSearchSource::GetResults, _shell_IOpenSearchSource_GetResults, shell.IOpenSearchSource_GetResults, shobjidl_core/IOpenSearchSource::GetResults
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOpenSearchSource::GetResults
 - shobjidl_core/IOpenSearchSource::GetResults
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IOpenSearchSource.GetResults
---

# IOpenSearchSource::GetResults


## -description

Returns search results, from an OpenSearch data source, formatted in RSS or Atom format.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

The window handle of the caller.

### -param pszQuery [in]

Type: <b>LPCWSTR</b>

The query as entered by the user. This parameter is equivalent to the OpenSearch {searchTerms} parameter and may be empty.

### -param dwStartIndex [in]

Type: <b>DWORD</b>

The index of the first result being requested. Equivalent to the OpenSearch {startIndex} parameter. See Remarks below.

### -param dwCount [in]

Type: <b>DWORD</b>

The number of results being requested.  Equivalent to the OpenSearch {count} parameter.

### -param riid [in]

Type: <b>REFIID</b>

The IID of the interface being requested. Typically IID_IStream.

### -param ppv [out]

Type: <b>void**</b>

An interface pointer, of type specified by RIID, to the object containing the results in Atom or RSS format.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. B_S_ENDOFROWSET optionally signifies the end of the results. The following errors display appropriate error messages in the info bar:
                

<ul>
<li>INET_E_AUTHENTICATION_REQUIRED (user does not have permission to access this resource)</li>
<li>INET_E_RESOURCE_NOT_FOUND (location was unavailable)</li>
<li>INET_E_DOWNLOAD_FAILURE (server error)</li>
</ul>

## -remarks

Windows Explorer calls this method with the search query parameters. The <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopensearchsource">IOpenSearchSource</a> implementation returns some or all results after performing required actions, such as providing custom authentication UI or connecting to the data source using a proprietary API.
            

<h3><a id="Paged_Results"></a><a id="paged_results"></a><a id="PAGED_RESULTS"></a>Paged Results</h3>
If you do not want the web service to return more than a limited number of results per request, this method can return just a "page" of results at a time. Windows Explorer can get additional pages of results by calling this method repeatedly and specifying a new index number. When returning results, the first result must be the result at the index requested by <i>dwStartIndex</i>.

<h3><a id="Index_Numbers_and_Counts"></a><a id="index_numbers_and_counts"></a><a id="INDEX_NUMBERS_AND_COUNTS"></a>Index Numbers and Counts</h3>
The index number identifies the first result on a page of results. It is equivalent to the OpenSearch {startIndex} parameter. The count, equivalent to the OpenSearch {count} parameter, identifies the expected or preferred number of items returned per page.

If a web service returns 20 items on the first page of results, the expected page size is 20.  To get the next 20 items, Windows Explorer would call <b>IOpenSearchSource::GetResults</b> with the value 21 for <i>dwStartIndex</i> and with the value of 20 for <i>dwCount</i>. When a page of results returned by the web service has fewer items than the expected page size, Windows Explorer assumes it has received the last page of results and stops making requests.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopensearchsource">IOpenSearchSource</a>