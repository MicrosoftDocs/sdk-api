---
UID: NF:wofapi.WofShouldCompressBinaries
title: WofShouldCompressBinaries function (wofapi.h)
description: Indicates whether compression should be used on a particular volume, and if so, which compression algorithm should be used.
helpviewer_keywords: ["WofShouldCompressBinaries","WofShouldCompressBinaries function [Files]","fs.wofshouldcompressbinaries","wofapi/WofShouldCompressBinaries"]
old-location: fs\wofshouldcompressbinaries.htm
tech.root: fs
ms.assetid: C7A1D76A-2535-46BB-A55B-D1E15A079FF4
ms.date: 12/05/2018
ms.keywords: WofShouldCompressBinaries, WofShouldCompressBinaries function [Files], fs.wofshouldcompressbinaries, wofapi/WofShouldCompressBinaries
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
 - WofShouldCompressBinaries
 - wofapi/WofShouldCompressBinaries
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
 - WofShouldCompressBinaries
---

# WofShouldCompressBinaries function


## -description

Indicates whether compression should be used on a particular volume, and if so, which compression algorithm should be used.

## -parameters

### -param Volume [in]

Specifies the path to the volume whose compression state is desired.

### -param Algorithm [out]

Points to a ULONG value. If the function returns TRUE, indicating compression is desired, this value will contain the algorithm that should be used for this volume.

## -returns

If binaries on this volume should be compressed, the return value is TRUE; otherwise it is FALSE. This function will return FALSE if the system does not support compression on the specified volume.

