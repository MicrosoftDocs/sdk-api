---
UID: NE:wuapi.tagDownloadPhase
title: tagDownloadPhase
author: windows-sdk-content
description: Defines the progress of the download of the current update that is returned by the CurrentUpdateDownloadPhase property of the IDownloadProgress interface.
old-location: wua\downloadphase.htm
old-project: wua_sdk
ms.assetid: a7e930dd-1dfa-42cc-9761-d4252c9a92ae
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DownloadPhase, DownloadPhase enumeration [Windows Update Agent], dphDownloading, dphInitializing, dphVerifying, tagDownloadPhase, wua.downloadphase, wuapi/DownloadPhase, wuapi/dphDownloading, wuapi/dphInitializing, wuapi/dphVerifying
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wuapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DownloadPhase
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wuapi.h
api_name:
 - DownloadPhase
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagDownloadPhase enumeration


## -description


Defines the progress of the download of the current update that is returned by the <a href="https://msdn.microsoft.com/5c94b0e9-c137-4677-a014-b8467a8049e5">CurrentUpdateDownloadPhase</a> property of the <a href="https://msdn.microsoft.com/773de760-5fde-4975-ba8d-d20b3affb4a7">IDownloadProgress</a> interface.


## -enum-fields




### -field dphInitializing

Initializing the download of the current update.


### -field dphDownloading

Downloading the current update.


### -field dphVerifying

Verifying the download of the current update.

