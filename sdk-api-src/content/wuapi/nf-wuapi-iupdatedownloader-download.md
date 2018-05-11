---
UID: NF:wuapi.IUpdateDownloader.Download
title: IUpdateDownloader::Download
author: windows-driver-content
description: Starts a synchronous download of the content files that are associated with the updates.
old-location: wua\iupdatedownloader_download.htm
old-project: Wua_Sdk
ms.assetid: 8b860632-3d10-4791-b4b3-d37aad319a0a
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: Download, Download method [Windows Update Agent], Download method [Windows Update Agent],IUpdateDownloader interface, IUpdateDownloader interface [Windows Update Agent],Download method, IUpdateDownloader.Download, IUpdateDownloader::Download, wua.iupdatedownloader_download, wuapi/IUpdateDownloader::Download
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: UpdateType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wuapi.dll
api_name:
-	IUpdateDownloader.Download
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateDownloader::Download


## -description


Starts a synchronous download of the content files that are associated with the updates.


## -parameters




### -param retval [out]

An <a href="https://msdn.microsoft.com/293bea59-acec-4774-adb9-1ad1d29406c3">IDownloadResult</a> interface that contains result codes for the download.


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
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_NO_UPDATE</b></dt>
</dl>
</td>
<td width="60%">
Windows Update Agent (WUA) does not have updates in the collection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
Windows Update Agent is not initialized.

</td>
</tr>
</table>
 




## -remarks



This method returns <b>WU_E_INVALID_OPERATION</b> if the object that is implementing the interface is locked down.

This method returns <b>WU_E_NO_UPDATE</b> if the <a href="https://msdn.microsoft.com/7c0444be-a9eb-461a-858e-1dea670afd06">Updates</a> property of the <a href="https://msdn.microsoft.com/8f9f3430-fc78-46cb-9dc8-b97e9d35d91c">IUpdateDownloader</a> interface is not set. This method also returns <b>WU_E_NO_UPDATE</b> if the <b>Updates</b> property is set to an empty collection.

This method returns <b>SUS_E_NOT_INITIALIZED</b> if the download job does not contain updates.




## -see-also




<a href="https://msdn.microsoft.com/8f9f3430-fc78-46cb-9dc8-b97e9d35d91c">IUpdateDownloader</a>
 

 

