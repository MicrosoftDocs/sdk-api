---
UID: NF:wuapi.IDownloadProgress.GetUpdateResult
title: IDownloadProgress::GetUpdateResult (wuapi.h)
description: Returns the result of the download of a specified update.
helpviewer_keywords: ["GetUpdateResult","GetUpdateResult method [Windows Update Agent]","GetUpdateResult method [Windows Update Agent]","IDownloadProgress interface","IDownloadProgress interface [Windows Update Agent]","GetUpdateResult method","IDownloadProgress.GetUpdateResult","IDownloadProgress::GetUpdateResult","wua.idownloadprogress_getupdateresult","wuapi/IDownloadProgress::GetUpdateResult"]
old-location: wua\idownloadprogress_getupdateresult.htm
tech.root: wua
ms.assetid: e7474a0a-98dc-4dd6-b5b8-8f88f0539f9a
ms.date: 12/05/2018
ms.keywords: GetUpdateResult, GetUpdateResult method [Windows Update Agent], GetUpdateResult method [Windows Update Agent],IDownloadProgress interface, IDownloadProgress interface [Windows Update Agent],GetUpdateResult method, IDownloadProgress.GetUpdateResult, IDownloadProgress::GetUpdateResult, wua.idownloadprogress_getupdateresult, wuapi/IDownloadProgress::GetUpdateResult
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
 - IDownloadProgress::GetUpdateResult
 - wuapi/IDownloadProgress::GetUpdateResult
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
 - IDownloadProgress.GetUpdateResult
---

# IDownloadProgress::GetUpdateResult


## -description

Returns the result of the download of a specified update.

## -parameters

### -param updateIndex [in]

A zero-based index value that specifies an update.

### -param retval [out]

An <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatedownloadresult">IUpdateDownloadResult</a> interface that contains information about the specified update.

## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-idownloadprogress">IDownloadProgress</a>