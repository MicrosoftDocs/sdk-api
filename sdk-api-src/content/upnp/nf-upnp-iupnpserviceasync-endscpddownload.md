---
UID: NF:upnp.IUPnPServiceAsync.EndSCPDDownload
title: IUPnPServiceAsync::EndSCPDDownload
author: windows-sdk-content
description: EndSCPDDownload method retrieves the results of a previous asynchronous download of an Service Control Protocol Description (SCPD) document.
old-location: upnp\iupnpserviceasync_endscpddownload.htm
old-project: upnp
ms.assetid: 1C4F7986-9282-4775-B9B2-338AC44F2243
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: EndSCPDDownload, EndSCPDDownload method [UPnP APIs], EndSCPDDownload method [UPnP APIs],IUPnPServiceAsync interface, IUPnPServiceAsync interface [UPnP APIs],EndSCPDDownload method, IUPnPServiceAsync.EndSCPDDownload, IUPnPServiceAsync::EndSCPDDownload, upnp.iupnpserviceasync_endscpddownload, upnp/IUPnPServiceAsync::EndSCPDDownload
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPServiceAsync.EndSCPDDownload
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnp.dll
req.irql: 
req.product: Windows UI
---

# IUPnPServiceAsync::EndSCPDDownload


## -description


The <b>EndSCPDDownload</b> method retrieves the results of  a previous asynchronous download of an Service Control Protocol Description (SCPD) document. 


## -parameters




### -param ullRequestID

Pointer to a 64-bit <b>ULONG</b> value that corresponds to the <a href="https://msdn.microsoft.com/CA573855-6D86-4C6C-B557-F8E8776BDBD3">BeginSCPDDownload</a> operation requested prior to this call.


### -param pbstrSCPDDoc [out]

A  buffer containing the SCPD document.


## -returns



Returns <b>S_OK</b> on success. Otherwise, the method returns a COM error code defined in <b>WinError.h</b> or one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failed to finalize the SCPD download and retrieve the document string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ullRequestID</i> does not match the pending async call.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/B77025D6-26C7-46C9-84FE-69685C61735D">IUPnPServiceAsync</a>



<a href="https://msdn.microsoft.com/CA573855-6D86-4C6C-B557-F8E8776BDBD3">IUPnPServiceAsync::BeginSCPDDownload</a>
 

 

