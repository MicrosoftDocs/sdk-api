---
UID: NF:wuapi.IUpdate.get_DownloadContents
title: IUpdate::get_DownloadContents (wuapi.h)
description: Gets file information about the download contents of the update.
helpviewer_keywords: ["DownloadContents property [Windows Update Agent]","DownloadContents property [Windows Update Agent]","IUpdate interface","IUpdate interface [Windows Update Agent]","DownloadContents property","IUpdate.DownloadContents","IUpdate.get_DownloadContents","IUpdate::DownloadContents","IUpdate::get_DownloadContents","get_DownloadContents","wua.iupdate_downloadcontents","wuapi/IUpdate::DownloadContents","wuapi/IUpdate::get_DownloadContents"]
old-location: wua\iupdate_downloadcontents.htm
tech.root: wua
ms.assetid: dbeeaac7-3841-42ec-a3f3-bdf94694dbef
ms.date: 12/05/2018
ms.keywords: DownloadContents property [Windows Update Agent], DownloadContents property [Windows Update Agent],IUpdate interface, IUpdate interface [Windows Update Agent],DownloadContents property, IUpdate.DownloadContents, IUpdate.get_DownloadContents, IUpdate::DownloadContents, IUpdate::get_DownloadContents, get_DownloadContents, wua.iupdate_downloadcontents, wuapi/IUpdate::DownloadContents, wuapi/IUpdate::get_DownloadContents
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
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
ms.custom: 19H1
f1_keywords:
 - IUpdate::get_DownloadContents
 - wuapi/IUpdate::get_DownloadContents
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
 - IUpdate.DownloadContents
 - IUpdate.get_DownloadContents
---

# IUpdate::get_DownloadContents


## -description

Gets file information about the download contents of the update.

This property is read-only.

## -parameters

### -param retval

An [IUpdateDownloadContentCollection](nn-wuapi-iupdatedownloadcontentcollection.md) that allows you to enumerate the URLs for download contents associated with an update.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>