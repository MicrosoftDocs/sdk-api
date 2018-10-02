---
UID: NF:wuapi.IUpdateDownloader.BeginDownload
title: IUpdateDownloader::BeginDownload
author: windows-sdk-content
description: Starts an asynchronous download of the content files that are associated with the updates.
old-location: wua\iupdatedownloader_begindownload.htm
tech.root: Wua_Sdk
ms.assetid: 9a953240-3d8e-4876-92a9-cc7efca62780
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: BeginDownload, BeginDownload method [Windows Update Agent], BeginDownload method [Windows Update Agent],IUpdateDownloader interface, IUpdateDownloader interface [Windows Update Agent],BeginDownload method, IUpdateDownloader.BeginDownload, IUpdateDownloader::BeginDownload, wua.iupdatedownloader_begindownload, wuapi/IUpdateDownloader::BeginDownload
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
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateDownloader.BeginDownload
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUpdateDownloader::BeginDownload


## -description


Starts an asynchronous download of the content files that are associated with the updates.


## -parameters




### -param onProgressChanged [in]

An <a href="https://msdn.microsoft.com/8fc414da-835c-438f-b607-8a273e7f9064">IDownloadProgressChangedCallback</a> interface that is called periodically for download progress changes before download is complete.


### -param onCompleted [in]

An <a href="https://msdn.microsoft.com/ad1c3075-21d9-409f-9677-fbf6d0c50313">IDownloadCompletedCallback</a> interface (C++/COM) that is called when an asynchronous download operation is complete.


### -param state [in]

The caller-specific state that the <a href="https://msdn.microsoft.com/47d2af4a-c04f-4413-ad29-3b8cb1292539">AsyncState</a> property of the <a href="https://msdn.microsoft.com/0157acab-53b6-43f9-a358-81cd5108c531">IDownloadJob</a> interface returns. A caller may use this parameter to attach a value to the download job object. This  allows the caller to retrieve custom information about that download job object at a later time.

<div class="alert"><b>Note</b>  <p class="note">The <a href="https://msdn.microsoft.com/47d2af4a-c04f-4413-ad29-3b8cb1292539">AsyncState</a> property of the <a href="https://msdn.microsoft.com/0157acab-53b6-43f9-a358-81cd5108c531">IDownloadJob</a> interface can be retrieved, but it cannot be set. This does not prevent the caller from changing the contents of the object already set to the <b>AsyncState</b> property of the <b>IDownloadJob</b> interface. In other words, if the <b>AsyncState</b> property contains a number, the number cannot be changed. But, if the <b>AsyncState</b> property contains a safe array or an object, the contents of the safe array or the object can be changed at will. The value is released when the caller releases <b>IDownloadJob</b> by calling <a href="https://msdn.microsoft.com/b89ec12a-8a51-46e6-9911-2535abc3925b">IUpdateDownloader::EndDownload</a>.

</div>
<div> </div>

### -param retval [out]

An <a href="https://msdn.microsoft.com/0157acab-53b6-43f9-a358-81cd5108c531">IDownloadJob</a> interface that contains the properties and methods that are available to a download operation that has started.


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
The Windows Update Agent (WUA) does not have  updates in the collection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The Windows Update Agent (WUA) is not initialized.

</td>
</tr>
</table>
 




## -remarks



  As an alternative to implementing the <a href="https://msdn.microsoft.com/8fc414da-835c-438f-b607-8a273e7f9064">IDownloadProgressChangedCallback</a> interface, you can use a script to   implement a callback routine of any identifier with DISPID 0 on an automation object. The type of the  <i>onProgressChanged</i> parameter is <b>IUnknown*</b>.

  As an alternative to implementing the <a href="https://msdn.microsoft.com/ad1c3075-21d9-409f-9677-fbf6d0c50313">IDownloadCompletedCallback</a> interface, you can use a script to   implement a callback routine of any identifier with DISPID 0 on an automation object. The type of the  <i>onCompleted</i> parameter is <b>IUnknown*</b>.

This method returns <b>WU_E_INVALID_OPERATION</b> if the object that is implementing the interface is  locked down.

This method returns <b>WU_E_NO_UPDATE</b> if the <a href="https://msdn.microsoft.com/7c0444be-a9eb-461a-858e-1dea670afd06">Updates</a> property of the <a href="https://msdn.microsoft.com/8f9f3430-fc78-46cb-9dc8-b97e9d35d91c">IUpdateDownloader</a> interface is not set. This method also returns WU_E_NO_UPDATE if the <b>Updates</b> property is set to an empty collection.

This method returns <b>SUS_E_NOT_INITIALIZED</b> if the download job contains no updates.

When you use any asynchronous WUA API in your app, you might need to implement a time-out mechanism. For more info about how to perform asynchronous WUA operations, see <a href="https://msdn.microsoft.com/1fb16904-732d-4341-8267-ab8896fc0f7c">Guidelines for Asynchronous WUA Operations</a>.





## -see-also




<a href="https://msdn.microsoft.com/8f9f3430-fc78-46cb-9dc8-b97e9d35d91c">IUpdateDownloader</a>
 

 

