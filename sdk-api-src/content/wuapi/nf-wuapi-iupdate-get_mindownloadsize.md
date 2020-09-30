---
UID: NF:wuapi.IUpdate.get_MinDownloadSize
title: IUpdate::get_MinDownloadSize (wuapi.h)
description: Gets the minimum download size of the update.
helpviewer_keywords: ["IUpdate interface [Windows Update Agent]","MinDownloadSize property","IUpdate.MinDownloadSize","IUpdate.get_MinDownloadSize","IUpdate::MinDownloadSize","IUpdate::get_MinDownloadSize","MinDownloadSize property [Windows Update Agent]","MinDownloadSize property [Windows Update Agent]","IUpdate interface","get_MinDownloadSize","wua.iupdate_mindownloadsize","wuapi/IUpdate::MinDownloadSize","wuapi/IUpdate::get_MinDownloadSize"]
old-location: wua\iupdate_mindownloadsize.htm
tech.root: wua
ms.assetid: 58666d64-fe29-4ece-8b51-67212f90e54e
ms.date: 12/05/2018
ms.keywords: IUpdate interface [Windows Update Agent],MinDownloadSize property, IUpdate.MinDownloadSize, IUpdate.get_MinDownloadSize, IUpdate::MinDownloadSize, IUpdate::get_MinDownloadSize, MinDownloadSize property [Windows Update Agent], MinDownloadSize property [Windows Update Agent],IUpdate interface, get_MinDownloadSize, wua.iupdate_mindownloadsize, wuapi/IUpdate::MinDownloadSize, wuapi/IUpdate::get_MinDownloadSize
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
 - IUpdate::get_MinDownloadSize
 - wuapi/IUpdate::get_MinDownloadSize
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
 - IUpdate.MinDownloadSize
 - IUpdate.get_MinDownloadSize
---

# IUpdate::get_MinDownloadSize


## -description

Gets the minimum download size of the update.

This property is read-only.

## -parameters

## -remarks

The <b>MinDownloadSize</b> property of an update is always downloaded.  However, the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_maxdownloadsize">MaxDownloadSize</a> property is not always downloaded. The <b>MaxDownloadSize</b> property is downloaded based on the configuration of the computer that receives the update.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>