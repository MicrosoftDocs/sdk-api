---
UID: NF:wofapi.WofWimUpdateEntry
title: WofWimUpdateEntry function
author: windows-sdk-content
description: Updates a WIM entry to point to a different WIM file location.
old-location: fs\wofwimupdateentry.htm
tech.root: FileIO
ms.assetid: 91CAE0F4-C0DB-40CE-BED9-C27E4856D4A0
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: WofWimUpdateEntry, WofWimUpdateEntry function [Files], fs.wofwimupdateentry, wofapi/WofWimUpdateEntry
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wofapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wofutil.lib
req.dll: Wofutil.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wofutil.dll
api_name:
 - WofWimUpdateEntry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WofWimUpdateEntry function


## -description


Updates a WIM entry to point to a different WIM file location.


## -parameters




### -param VolumeName [in]

The volume name which contains files whose data is provided by the WIM.


### -param DataSourceId [in]

Identifies the WIM entry.


### -param NewWimPath [in]

The new location of the WIM file.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



