---
UID: NF:wuapi.IUpdateDownloader.put_IsForced
title: IUpdateDownloader::put_IsForced (wuapi.h)
description: Gets and sets a Boolean value that indicates whether the Windows Update Agent (WUA) forces the download of updates that are already installed or that cannot be installed. (Put)
helpviewer_keywords: ["IUpdateDownloader interface [Windows Update Agent]","IsForced property","IUpdateDownloader.IsForced","IUpdateDownloader.put_IsForced","IUpdateDownloader::IsForced","IUpdateDownloader::get_IsForced","IUpdateDownloader::put_IsForced","IsForced property [Windows Update Agent]","IsForced property [Windows Update Agent]","IUpdateDownloader interface","put_IsForced","wua.iupdatedownloader_isforced","wuapi/IUpdateDownloader::IsForced","wuapi/IUpdateDownloader::get_IsForced","wuapi/IUpdateDownloader::put_IsForced"]
old-location: wua\iupdatedownloader_isforced.htm
tech.root: wua
ms.assetid: e1ac3da4-341c-4a4e-920f-b84af03e324e
ms.date: 12/05/2018
ms.keywords: IUpdateDownloader interface [Windows Update Agent],IsForced property, IUpdateDownloader.IsForced, IUpdateDownloader.put_IsForced, IUpdateDownloader::IsForced, IUpdateDownloader::get_IsForced, IUpdateDownloader::put_IsForced, IsForced property [Windows Update Agent], IsForced property [Windows Update Agent],IUpdateDownloader interface, put_IsForced, wua.iupdatedownloader_isforced, wuapi/IUpdateDownloader::IsForced, wuapi/IUpdateDownloader::get_IsForced, wuapi/IUpdateDownloader::put_IsForced
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
 - IUpdateDownloader::put_IsForced
 - wuapi/IUpdateDownloader::put_IsForced
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
 - IUpdateDownloader.IsForced
 - IUpdateDownloader.get_IsForced
 - IUpdateDownloader.put_IsForced
---

# IUpdateDownloader::put_IsForced


## -description

Gets and sets a Boolean value that indicates whether the  Windows Update Agent (WUA) forces the download of  updates that are already installed or that cannot be installed.

This property is read/write.

## -parameters

## -remarks

This method returns <b>WU_E_INVALID_OPERATION</b> if the object that is implementing the interface is locked down.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatedownloader">IUpdateDownloader</a>
