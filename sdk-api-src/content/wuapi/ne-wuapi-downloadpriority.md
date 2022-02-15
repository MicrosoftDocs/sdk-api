---
UID: NE:wuapi.tagDownloadPriority
title: DownloadPriority (wuapi.h)
description: Defines the possible priorities for a download operation.
helpviewer_keywords: ["DownloadPriority","DownloadPriority enumeration [Windows Update Agent]","dpHigh","dpLow","dpNormal","wua.downloadpriority","wuapi/DownloadPriority","wuapi/dpHigh","wuapi/dpLow","wuapi/dpNormal"]
old-location: wua\downloadpriority.htm
tech.root: wua
ms.assetid: 6e70c513-861b-4a7f-a613-09ba2ef64bf1
ms.date: 12/05/2018
ms.keywords: DownloadPriority, DownloadPriority enumeration [Windows Update Agent], dpHigh, dpLow, dpNormal, wua.downloadpriority, wuapi/DownloadPriority, wuapi/dpHigh, wuapi/dpLow, wuapi/dpNormal
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
req.typenames: DownloadPriority
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDownloadPriority
 - wuapi/tagDownloadPriority
 - DownloadPriority
 - wuapi/DownloadPriority
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
 - DownloadPriority
---

# DownloadPriority enumeration


## -description

Defines the possible priorities for a download operation.

## -enum-fields

### -field dpLow:1

Updates are downloaded as low priority.

### -field dpNormal:2

Updates are downloaded as normal priority.

### -field dpHigh:3

Updates are downloaded as high priority.

### -field dpExtraHigh:4

