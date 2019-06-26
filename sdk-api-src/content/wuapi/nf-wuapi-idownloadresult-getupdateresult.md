---
UID: NF:wuapi.IDownloadResult.GetUpdateResult
title: IDownloadResult::GetUpdateResult (wuapi.h)
author: windows-sdk-content
description: Returns an IUpdateDownloadResult interface that contains the download information for a specified update.
old-location: wua\idownloadresult_getupdateresult.htm
tech.root: Wua_Sdk
ms.assetid: d95ce8ad-74d7-4144-9a4b-75d69d5a9442
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetUpdateResult, GetUpdateResult method [Windows Update Agent], GetUpdateResult method [Windows Update Agent],IDownloadResult interface, IDownloadResult interface [Windows Update Agent],GetUpdateResult method, IDownloadResult.GetUpdateResult, IDownloadResult::GetUpdateResult, wua.idownloadresult_getupdateresult, wuapi/IDownloadResult::GetUpdateResult
ms.topic: method
f1_keywords: 
 - "wuapi/IDownloadResult.GetUpdateResult"
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
 - IDownloadResult.GetUpdateResult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDownloadResult::GetUpdateResult


## -description


Returns an <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdatedownloadresult">IUpdateDownloadResult</a> interface that contains the download information for a specified update.


## -parameters




### -param updateIndex [in]

The index of the update.


### -param retval [out]

An <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdatedownloadresult">IUpdateDownloadResult</a> interface that contains the results for the specified update.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns  a COM or Windows 

error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-idownloadresult">IDownloadResult</a>
 

 

