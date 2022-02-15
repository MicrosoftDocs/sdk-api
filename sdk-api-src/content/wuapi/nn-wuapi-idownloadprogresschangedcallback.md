---
UID: NN:wuapi.IDownloadProgressChangedCallback
title: IDownloadProgressChangedCallback (wuapi.h)
description: Handles the notification that indicates a change in the progress of an asynchronous download operation.
helpviewer_keywords: ["IDownloadProgressChangedCallback","IDownloadProgressChangedCallback interface [Windows Update Agent]","IDownloadProgressChangedCallback interface [Windows Update Agent]","described","wua.idownloadprogresschangedcallback","wuapi/IDownloadProgressChangedCallback"]
old-location: wua\idownloadprogresschangedcallback.htm
tech.root: wua
ms.assetid: 8fc414da-835c-438f-b607-8a273e7f9064
ms.date: 12/05/2018
ms.keywords: IDownloadProgressChangedCallback, IDownloadProgressChangedCallback interface [Windows Update Agent], IDownloadProgressChangedCallback interface [Windows Update Agent],described, wua.idownloadprogresschangedcallback, wuapi/IDownloadProgressChangedCallback
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
 - IDownloadProgressChangedCallback
 - wuapi/IDownloadProgressChangedCallback
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
 - IDownloadProgressChangedCallback
---

# IDownloadProgressChangedCallback interface


## -description

Handles the notification that indicates a change in the progress of an asynchronous download operation.   This interface is implemented by programmers who call the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatedownloader-begindownload">IUpdateDownloader.BeginDownload</a> method.

## -inheritance

The <b>IDownloadProgressChangedCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDownloadProgressChangedCallback</b> also has these types of members:

