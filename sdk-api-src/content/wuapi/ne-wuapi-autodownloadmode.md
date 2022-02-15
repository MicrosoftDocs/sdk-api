---
UID: NE:wuapi.tagAutoDownloadMode
title: AutoDownloadMode (wuapi.h)
description: Defines the types of logic that is used to determine whether Automatic Updates will automatically download an update once it is determined to be applicable for the computer.
helpviewer_keywords: ["AutoDownloadMode","AutoDownloadMode enumeration [Windows Update Agent]","adAlwaysAutoDownload","adLetWindowsUpdateDecide","adNeverAutoDownload","wua.autodownloadmode","wuapi/AutoDownloadMode","wuapi/adAlwaysAutoDownload","wuapi/adLetWindowsUpdateDecide","wuapi/adNeverAutoDownload"]
old-location: wua\autodownloadmode.htm
tech.root: wua
ms.assetid: cabf21b8-790b-401b-9de2-0d8c5fa858e1
ms.date: 12/05/2018
ms.keywords: AutoDownloadMode, AutoDownloadMode enumeration [Windows Update Agent], adAlwaysAutoDownload, adLetWindowsUpdateDecide, adNeverAutoDownload, wua.autodownloadmode, wuapi/AutoDownloadMode, wuapi/adAlwaysAutoDownload, wuapi/adLetWindowsUpdateDecide, wuapi/adNeverAutoDownload
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
req.typenames: AutoDownloadMode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagAutoDownloadMode
 - wuapi/tagAutoDownloadMode
 - AutoDownloadMode
 - wuapi/AutoDownloadMode
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
 - AutoDownloadMode
---

# AutoDownloadMode enumeration


## -description

Defines the types of logic that is used to determine whether Automatic Updates will automatically download an update once it is determined to be applicable for the computer.

## -enum-fields

### -field adLetWindowsUpdateDecide:0

Use the standard logic. The update will be automatically downloaded if it is important, or if it is recommended and Windows Update has been configured to treat recommended updates as important. Otherwise, the update will not be automatically downloaded.

### -field adNeverAutoDownload:1

The update will not be automatically downloaded; it will  be downloaded only when the user attempts to install the update, or when a Windows Update Agent (WUA) API caller requests that the update be downloaded by using the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatedownloader-download">IUpdateDownloader::Download</a> or <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatedownloader-begindownload">IUpdateDownloader::BeginDownload</a> methods.

### -field adAlwaysAutoDownload:2

The update will always be automatically downloaded.

## -remarks

If Automatic Updates is disabled, or if Automatic Updates is enabled but set to “Check for updates but let me choose whether to download or install them,” updates will never be automatically downloaded, regardless of the value of an update’s <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdate5-get_autodownload">IUpdate5::AutoDownload</a> property. In earlier versions of the WUA in which <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate5">IUpdate5</a> is not available, all updates are processed by using the standard logic.
