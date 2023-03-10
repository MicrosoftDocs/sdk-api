---
UID: NE:wuapi.tagDownloadPhase
title: DownloadPhase (wuapi.h)
description: Defines the progress of the download of the current update that is returned by the CurrentUpdateDownloadPhase property of the IDownloadProgress interface.
helpviewer_keywords: ["DownloadPhase","DownloadPhase enumeration [Windows Update Agent]","dphDownloading","dphInitializing","dphVerifying","wua.downloadphase","wuapi/DownloadPhase","wuapi/dphDownloading","wuapi/dphInitializing","wuapi/dphVerifying"]
old-location: wua\downloadphase.htm
tech.root: wua
ms.assetid: a7e930dd-1dfa-42cc-9761-d4252c9a92ae
ms.date: 12/05/2018
ms.keywords: DownloadPhase, DownloadPhase enumeration [Windows Update Agent], dphDownloading, dphInitializing, dphVerifying, wua.downloadphase, wuapi/DownloadPhase, wuapi/dphDownloading, wuapi/dphInitializing, wuapi/dphVerifying
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DownloadPhase
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDownloadPhase
 - wuapi/tagDownloadPhase
 - DownloadPhase
 - wuapi/DownloadPhase
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wuapi.h
api_name:
 - DownloadPhase
---

# DownloadPhase enumeration


## -description

Defines the progress of the download of the current update that is returned by the <a href="/windows/desktop/api/wuapi/nf-wuapi-idownloadprogress-get_currentupdatedownloadphase">CurrentUpdateDownloadPhase</a> property of the <a href="/windows/desktop/api/wuapi/nn-wuapi-idownloadprogress">IDownloadProgress</a> interface.

## -enum-fields

### -field dphInitializing:1

Initializing the download of the current update.

### -field dphDownloading:2

Downloading the current update.

### -field dphVerifying:3

Verifying the download of the current update.
