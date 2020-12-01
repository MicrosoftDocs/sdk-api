---
UID: NF:wuapi.IUpdate.get_MaxDownloadSize
title: IUpdate::get_MaxDownloadSize (wuapi.h)
description: Gets the maximum download size of the update.
helpviewer_keywords: ["IUpdate interface [Windows Update Agent]","MaxDownloadSize property","IUpdate.MaxDownloadSize","IUpdate.get_MaxDownloadSize","IUpdate::MaxDownloadSize","IUpdate::get_MaxDownloadSize","MaxDownloadSize property [Windows Update Agent]","MaxDownloadSize property [Windows Update Agent]","IUpdate interface","get_MaxDownloadSize","wua.iupdate_maxdownloadsize","wuapi/IUpdate::MaxDownloadSize","wuapi/IUpdate::get_MaxDownloadSize"]
old-location: wua\iupdate_maxdownloadsize.htm
tech.root: wua
ms.assetid: 22f19d4f-e144-4b06-a428-d2133198288a
ms.date: 12/05/2018
ms.keywords: IUpdate interface [Windows Update Agent],MaxDownloadSize property, IUpdate.MaxDownloadSize, IUpdate.get_MaxDownloadSize, IUpdate::MaxDownloadSize, IUpdate::get_MaxDownloadSize, MaxDownloadSize property [Windows Update Agent], MaxDownloadSize property [Windows Update Agent],IUpdate interface, get_MaxDownloadSize, wua.iupdate_maxdownloadsize, wuapi/IUpdate::MaxDownloadSize, wuapi/IUpdate::get_MaxDownloadSize
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
 - IUpdate::get_MaxDownloadSize
 - wuapi/IUpdate::get_MaxDownloadSize
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
 - IUpdate.MaxDownloadSize
 - IUpdate.get_MaxDownloadSize
---

# IUpdate::get_MaxDownloadSize


## -description

Gets the maximum download size of the update.

This property is read-only.

## -parameters

## -remarks

The <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_mindownloadsize">MinDownloadSize</a> property of an update is always downloaded.  However, the <b>MaxDownloadSize</b> property is not always downloaded. The <b>MaxDownloadSize</b> property is downloaded based on the configuration of the computer that receives the update.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>