---
UID: NF:wuapi.IDownloadProgress.GetUpdateResult
title: IDownloadProgress::GetUpdateResult
author: windows-sdk-content
description: Returns the result of the download of a specified update.
old-location: wua\idownloadprogress_getupdateresult.htm
tech.root: Wua_Sdk
ms.assetid: e7474a0a-98dc-4dd6-b5b8-8f88f0539f9a
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetUpdateResult, GetUpdateResult method [Windows Update Agent], GetUpdateResult method [Windows Update Agent],IDownloadProgress interface, IDownloadProgress interface [Windows Update Agent],GetUpdateResult method, IDownloadProgress.GetUpdateResult, IDownloadProgress::GetUpdateResult, wua.idownloadprogress_getupdateresult, wuapi/IDownloadProgress::GetUpdateResult
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
 - IDownloadProgress.GetUpdateResult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDownloadProgress::GetUpdateResult


## -description


Returns the result of the download of a specified update.


## -parameters




### -param updateIndex [in]

A zero-based index value that specifies an update.


### -param retval [out]

An <a href="https://msdn.microsoft.com/d2a800c9-c23a-4aab-a9c6-e408349818dd">IUpdateDownloadResult</a> interface that contains information about the specified update.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.




## -see-also




<a href="https://msdn.microsoft.com/773de760-5fde-4975-ba8d-d20b3affb4a7">IDownloadProgress</a>
 

 

