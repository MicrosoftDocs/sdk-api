---
UID: NF:wofapi.WofWimUpdateEntry
title: WofWimUpdateEntry function (wofapi.h)
description: Updates a WIM entry to point to a different WIM file location.
helpviewer_keywords: ["WofWimUpdateEntry","WofWimUpdateEntry function [Files]","fs.wofwimupdateentry","wofapi/WofWimUpdateEntry"]
old-location: fs\wofwimupdateentry.htm
tech.root: fs
ms.assetid: 91CAE0F4-C0DB-40CE-BED9-C27E4856D4A0
ms.date: 12/05/2018
ms.keywords: WofWimUpdateEntry, WofWimUpdateEntry function [Files], fs.wofwimupdateentry, wofapi/WofWimUpdateEntry
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WofWimUpdateEntry
 - wofapi/WofWimUpdateEntry
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wofutil.dll
api_name:
 - WofWimUpdateEntry
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

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

