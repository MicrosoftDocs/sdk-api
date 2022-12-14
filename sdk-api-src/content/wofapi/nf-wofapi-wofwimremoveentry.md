---
UID: NF:wofapi.WofWimRemoveEntry
title: WofWimRemoveEntry function (wofapi.h)
description: Removes a single WIM data source from backing files on a volume.
helpviewer_keywords: ["WofWimRemoveEntry","WofWimRemoveEntry function [Files]","fs.wofwimremoveentry","wofapi/WofWimRemoveEntry"]
old-location: fs\wofwimremoveentry.htm
tech.root: fs
ms.assetid: B376EDF7-8C46-4C8B-900E-0DC79699EC1E
ms.date: 12/05/2018
ms.keywords: WofWimRemoveEntry, WofWimRemoveEntry function [Files], fs.wofwimremoveentry, wofapi/WofWimRemoveEntry
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
 - WofWimRemoveEntry
 - wofapi/WofWimRemoveEntry
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
 - WofWimRemoveEntry
---

# WofWimRemoveEntry function


## -description

Removes a single WIM data source from backing files on a volume.

## -parameters

### -param VolumeName [in]

The volume name which contained files whose data was provided by the WIM.

### -param DataSourceId [in]

Identifies the WIM entry.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the volume currently has files whose data is derived from the WIM file, the data for those files will become permanently inaccessible. It is good practice to remove any files referring to the WIM file prior to removing the data source from a volume.  Once all data sources for a WIM file have been removed, the WIM file itself can be renamed or deleted.

## -see-also

<a href="/windows-hardware/drivers/ifs/fsctl-remove-overlay">FSCTL_REMOVE_OVERLAY</a>