---
UID: NF:wuapi.IUpdateDownloader.EndDownload
title: IUpdateDownloader::EndDownload
author: windows-sdk-content
description: Completes an asynchronous download.
old-location: wua\iupdatedownloader_enddownload.htm
old-project: Wua_Sdk
ms.assetid: b89ec12a-8a51-46e6-9911-2535abc3925b
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: EndDownload, EndDownload method [Windows Update Agent], EndDownload method [Windows Update Agent],IUpdateDownloader interface, IUpdateDownloader interface [Windows Update Agent],EndDownload method, IUpdateDownloader.EndDownload, IUpdateDownloader::EndDownload, wua.iupdatedownloader_enddownload, wuapi/IUpdateDownloader::EndDownload
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: UpdateType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wuapi.dll
api_name:
-	IUpdateDownloader.EndDownload
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateDownloader::EndDownload


## -description


Completes an asynchronous download.


## -parameters




### -param value [in]

The <a href="https://msdn.microsoft.com/0157acab-53b6-43f9-a358-81cd5108c531">IDownloadJob</a> interface pointer that  <a href="https://msdn.microsoft.com/9a953240-3d8e-4876-92a9-cc7efca62780">BeginDownload</a> returns.


### -param retval [out]

An <a href="https://msdn.microsoft.com/293bea59-acec-4774-adb9-1ad1d29406c3">IDownloadResult</a> interface that contains result codes for a download.


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

When you use any asynchronous WUA API in your app, you might need to implement a time-out mechanism. For more info about how to perform asynchronous WUA operations, see <a href="https://msdn.microsoft.com/1fb16904-732d-4341-8267-ab8896fc0f7c">Guidelines for Asynchronous WUA Operations</a>.





## -see-also




<a href="https://msdn.microsoft.com/8f9f3430-fc78-46cb-9dc8-b97e9d35d91c">IUpdateDownloader</a>
 

 

