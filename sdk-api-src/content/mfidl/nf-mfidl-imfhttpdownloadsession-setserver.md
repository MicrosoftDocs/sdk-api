---
UID: NF:mfidl.IMFHttpDownloadSession.SetServer
title: IMFHttpDownloadSession::SetServer
author: windows-sdk-content
description: Called by Microsoft Media Foundation to specify parameters common to all requests created by this instance of IMFHttpDownloadSession.
old-location: mf\imfhttpdownloadsession_setserver.htm
old-project: medfound
ms.assetid: 408D4863-D95F-4BBD-9F0B-9796ED08A256
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMFHttpDownloadSession interface [Media Foundation],SetServer method, IMFHttpDownloadSession.SetServer, IMFHttpDownloadSession::SetServer, SetServer, SetServer method [Media Foundation], SetServer method [Media Foundation],IMFHttpDownloadSession interface, mf.imfhttpdownloadsession_setserver, mfidl/IMFHttpDownloadSession::SetServer
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
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
-	IMFHttpDownloadSession.SetServer
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFHttpDownloadSession::SetServer


## -description


Called  by Microsoft Media Foundation to specify parameters common to all requests created by this instance of <a href="https://msdn.microsoft.com/048B2922-3B77-4F2D-9437-0FA54F94C67E">IMFHttpDownloadSession</a>.


## -parameters




### -param szServerName [in]

The host name, fully qualified DNS name, or IP address of the HTTP server that the requests shall be sent to.


### -param nPort [in]

The TCP port number of the server.


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

                Successfully stored the supplied data.

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




<a href="https://msdn.microsoft.com/048B2922-3B77-4F2D-9437-0FA54F94C67E">IMFHttpDownloadSession</a>
 

 

