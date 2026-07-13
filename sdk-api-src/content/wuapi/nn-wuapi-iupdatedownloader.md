---
UID: NN:wuapi.IUpdateDownloader
title: IUpdateDownloader (wuapi.h)
description: Downloads updates from the server.
helpviewer_keywords: ["IUpdateDownloader","IUpdateDownloader interface [Windows Update Agent]","IUpdateDownloader interface [Windows Update Agent]","described","wua.iupdatedownloader","wuapi/IUpdateDownloader"]
old-location: wua\iupdatedownloader.htm
tech.root: wua
ms.assetid: 8f9f3430-fc78-46cb-9dc8-b97e9d35d91c
ms.date: 12/05/2018
ms.keywords: IUpdateDownloader, IUpdateDownloader interface [Windows Update Agent], IUpdateDownloader interface [Windows Update Agent],described, wua.iupdatedownloader, wuapi/IUpdateDownloader
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
 - IUpdateDownloader
 - wuapi/IUpdateDownloader
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
 - IUpdateDownloader
---

# IUpdateDownloader interface


## -description

Downloads updates from the server.

## -inheritance

The <b>IUpdateDownloader</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IUpdateDownloader</b> also has these types of members:

## -remarks

You can create an instance of this interface by using the UpdateDownloader coclass. Use the Microsoft.Update.Downloader program identifier to create the object.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
