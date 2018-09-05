---
UID: NF:webservices.WsReadMetadata
title: WsReadMetadata function
author: windows-sdk-content
description: Reads a Metadata element and adds it to the Metadata documents of the Metadata object.
old-location: wsw\wsreadmetadata.htm
old-project: wsw
ms.assetid: 0b824948-e06d-482d-8d53-c4e27d1ecf0f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WsReadMetadata, WsReadMetadata function [Web Services for Windows], webservices/WsReadMetadata, wsw.wsreadmetadata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: webservices.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsReadMetadata
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsReadMetadata function


## -description


Reads a Metadata element and adds it to the Metadata
                documents of the Metadata object.
            
                The Metadata object state must be set to <b>WS_METADATA_STATE_CREATED</b>.
            On error the Metadata
                object state is reset to <b>WS_METADATA_STATE_FAULTED</b>.
            <div class="alert"><b>Note</b>  The function will consume an element if the element contains metadata.  If the element is not recognized as containing
                metadata, or the particular type of metadata is not needed, 
                the element it is not read.
            </div>
<div> </div>



## -parameters




### -param metadata [in]

A pointer to the <b>Metadata</b> object for storing the metadata read.  The pointer must reference a valid <a href="https://msdn.microsoft.com/aa7383a1-60fa-448a-b0c6-b9c49d9d5070">WS_METADATA</a> object.
                


### -param reader [in]

A pointer to the <b>XML Reader</b> object used to read the metadata.  The pointer must reference a valid <a href="https://msdn.microsoft.com/7acbe407-e91b-435a-82bc-acbbc13cfcfd">WS_XML_READER</a> object and the reader must be positioned
                    on the element containing the desired metadata.
                


### -param url [in]

A pointer to 
                    a <a href="https://msdn.microsoft.com/eb6c7397-6b15-4e79-89ec-585861113edf">WS_STRING</a> object referencing the retrieved metadata URL.  The URL is
                    used to track the metadata documents for resolving URL-based
                    links between documents.
                <div class="alert"><b>Note</b>  The URL MUST be fully qualified.  The URL can have a fragment identifier.
                </div>
<div> </div>


The following URL schemes are supported:
                

<ul>
<li><b>WS_URL_HTTP_SCHEME_TYPE</b></li>
<li><b>WS_URL_HTTPS_SCHEME_TYPE</b></li>
<li><b>WS_URL_NETTCP_SCHEME_TYPE</b></li>
</ul>
Each URL specified using this function must have a 
                    unique base URL.  The base URL is computed by
                    removing any fragment identifier from the URL specified.
                    For example if the following URLs were specified:
                

<pre class="syntax" xml:space="preserve"><code>
http://example.com/document1#fragment
http://example.com/document2
</code></pre>
The two base URLs would be:
                

<pre class="syntax" xml:space="preserve"><code>
http://example.com/document1
http://example.com/document2
</code></pre>

### -param error [in, optional]

A  pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object where additional information about the error should be stored if the function fails.
                


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The input data was not in the expected format or did not have the expected value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The operation is not allowed due to the current state of the object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
A quota was exceeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Ran out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The element was not consumed.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>
 




## -remarks



This function recognizes the following types of metadata:
            

<ul>
<li>WSDL 1.1 documents
                </li>
<li>WS-Policy 1.2 documents </li>
</ul>


