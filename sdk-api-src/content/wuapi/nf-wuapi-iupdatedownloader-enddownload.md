---
UID: NF:wuapi.IUpdateDownloader.EndDownload
title: IUpdateDownloader::EndDownload (wuapi.h)
description: Completes an asynchronous download.
helpviewer_keywords: ["EndDownload","EndDownload method [Windows Update Agent]","EndDownload method [Windows Update Agent]","IUpdateDownloader interface","IUpdateDownloader interface [Windows Update Agent]","EndDownload method","IUpdateDownloader.EndDownload","IUpdateDownloader::EndDownload","wua.iupdatedownloader_enddownload","wuapi/IUpdateDownloader::EndDownload"]
old-location: wua\iupdatedownloader_enddownload.htm
tech.root: wua
ms.assetid: b89ec12a-8a51-46e6-9911-2535abc3925b
ms.date: 12/05/2018
ms.keywords: EndDownload, EndDownload method [Windows Update Agent], EndDownload method [Windows Update Agent],IUpdateDownloader interface, IUpdateDownloader interface [Windows Update Agent],EndDownload method, IUpdateDownloader.EndDownload, IUpdateDownloader::EndDownload, wua.iupdatedownloader_enddownload, wuapi/IUpdateDownloader::EndDownload
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUpdateDownloader::EndDownload
 - wuapi/IUpdateDownloader::EndDownload
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateDownloader.EndDownload
---

# IUpdateDownloader::EndDownload


## -description

Completes an asynchronous download.

## -parameters

### -param value [in]

The <a href="/windows/desktop/api/wuapi/nn-wuapi-idownloadjob">IDownloadJob</a> interface pointer that  <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatedownloader-begindownload">BeginDownload</a> returns.

### -param retval [out]

An <a href="/windows/desktop/api/wuapi/nn-wuapi-idownloadresult">IDownloadResult</a> interface that contains result codes for a download.

## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code. 

This method can also return the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The computer cannot access the update site.

</td>
</tr>
</table>

## -remarks

This method returns <b>WU_E_INVALID_OPERATION</b> if the object that is implementing the interface is locked down.

When you use any asynchronous WUA API in your app, you might need to implement a time-out mechanism. For more info about how to perform asynchronous WUA operations, see <a href="/windows/desktop/Wua_Sdk/guidelines-for-asynchronous-wua-operations">Guidelines for Asynchronous WUA Operations</a>.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatedownloader">IUpdateDownloader</a>