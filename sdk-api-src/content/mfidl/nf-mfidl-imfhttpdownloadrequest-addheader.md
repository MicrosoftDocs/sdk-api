---
UID: NF:mfidl.IMFHttpDownloadRequest.AddHeader
title: IMFHttpDownloadRequest::AddHeader
author: windows-driver-content
description: Invoked by Microsoft Media Foundation to add a single HTTP header to a HTTP request. Microsoft Media Foundation will invoke this method once for each header that shall be included in the HTTP request, before it invokes the BeginSendRequest method.
old-location: mf\imfhttpdownloadrequest_addheader.htm
old-project: medfound
ms.assetid: 37A2C9D8-EFF6-49D5-B495-EDBEEABD59CE
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: AddHeader, AddHeader method [Media Foundation], AddHeader method [Media Foundation],IMFHttpDownloadRequest interface, IMFHttpDownloadRequest interface [Media Foundation],AddHeader method, IMFHttpDownloadRequest.AddHeader, IMFHttpDownloadRequest::AddHeader, mf.imfhttpdownloadrequest_addheader, mfidl/IMFHttpDownloadRequest::AddHeader
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
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfplat.lib
-	mfplat.dll
-	mfplat.dll
-	mfplat.dll.dll
api_name:
-	IMFHttpDownloadRequest.AddHeader
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFHttpDownloadRequest::AddHeader


## -description


Invoked by Microsoft Media Foundation to add a single HTTP header to a HTTP request.  Microsoft Media Foundation will invoke this method once for each header that shall be included in the HTTP request, before it invokes the <a href="https://msdn.microsoft.com/38025B19-146A-4050-9BD2-2CF974729FE3">BeginSendRequest</a> method.


## -parameters




### -param szHeader [in]

Contains a single HTTP request header, for example, “Accept: */*”. The string does not include the carriage return or line feed characters.


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

                Successfully added the header to the list of headers to be sent with the request.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/A8A37C2F-A662-4FDA-95F6-43D96A8471A8">IMFHttpDownloadRequest</a>
 

 

