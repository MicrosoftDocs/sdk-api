---
UID: NF:mfidl.IMFHttpDownloadSession.CreateRequest
title: IMFHttpDownloadSession::CreateRequest
author: windows-sdk-content
description: Invoked by Microsoft Media Foundation to create an object that implements the IMFHttpDownloadRequest interface, which is used to send a single HTTP, or HTTPS request.
old-location: mf\imfhttpdownloadsession_createrequest.htm
tech.root: medfound
ms.assetid: 111A075A-82A7-4607-9359-37B2DA97AFC5
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: CreateRequest, CreateRequest method [Media Foundation], CreateRequest method [Media Foundation],IMFHttpDownloadSession interface, IMFHttpDownloadSession interface [Media Foundation],CreateRequest method, IMFHttpDownloadSession.CreateRequest, IMFHttpDownloadSession::CreateRequest, mf.imfhttpdownloadsession_createrequest, mfidl/IMFHttpDownloadSession::CreateRequest
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFHttpDownloadSession.CreateRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFHttpDownloadSession::CreateRequest


## -description


Invoked by Microsoft Media Foundation to create an object that implements the <a href="https://msdn.microsoft.com/A8A37C2F-A662-4FDA-95F6-43D96A8471A8">IMFHttpDownloadRequest</a> interface, which is used to send a single HTTP, or HTTPS request. Since multiple requests may be needed to fully download a resource, Media Foundation may invoke <b>CreateRequest</b> multiple times on the same <a href="https://msdn.microsoft.com/048B2922-3B77-4F2D-9437-0FA54F94C67E">IMFHttpDownloadSession</a> instance. Media Foundation will use each <b>IMFHttpDownloadRequest</b> instance for only a single request. 


## -parameters




### -param szObjectName [in]

Pointer to a string that contains the name of the target resource of the specified HTTP verb. This is generally a file name, an executable module, or a search specifier. The target resource always begins with a forward slash character and includes any query string that was included on the URL.


### -param fBypassProxyCache [in]

If set to TRUE, indicates that the request should be forwarded to the originating server rather than sending a cached version of a resource from a proxy server. When this flag is set to TRUE, a "Pragma: no-cache" header should be added to the request. When creating an HTTP/1.1 request, a "Cache-Control: no-cache" should also be added.


### -param fSecure [in]

If set to TRUE, causes the secure variant of the protocol to be used, if applicable. For example, if the <a href="https://msdn.microsoft.com/048B2922-3B77-4F2D-9437-0FA54F94C67E">IMFHttpDownloadSession</a> is for HTTP/HTTPS, setting <i>fSecure</i> to TRUE will cause the request to use HTTPS. Otherwise, the unsecure variant of the protocol (in this example, HTTP) is used.


### -param szVerb [in, optional]

Pointer to a string that contains the HTTP verb to use in the request. If this parameter is NULL, the function uses GET as the HTTP verb. 

<div class="alert"><b>Note</b>  This string should be all uppercase. Many servers treat HTTP verbs as case-sensitive, and the Internet Engineering Task Force (IETF) Requests for Comments (RFCs) spell these verbs using uppercase characters only.</div>
<div> </div>

### -param szReferrer [in, optional]

Pointer to a string that specifies the URL of the document from which the URL in the request <i>szObjectName</i> was obtained. If this parameter is set to NULL, no referring document is specified.


### -param ppRequest

Upon successful return of the method, this parameter is set to an <a href="https://msdn.microsoft.com/A8A37C2F-A662-4FDA-95F6-43D96A8471A8">IMFHttpDownloadRequest</a> interface. 


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Successfully stored the supplied information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The method was invoked after <a href="https://msdn.microsoft.com/587D281D-0488-470B-9E20-AE6DE70F33DC">Close</a> or before <a href="https://msdn.microsoft.com/408D4863-D95F-4BBD-9F0B-9796ED08A256">SetServer</a> was invoked.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/048B2922-3B77-4F2D-9437-0FA54F94C67E">IMFHttpDownloadSession</a>
 

 

