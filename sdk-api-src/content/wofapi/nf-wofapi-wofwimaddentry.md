---
UID: NF:wofapi.WofWimAddEntry
title: WofWimAddEntry function (wofapi.h)
description: Adds a single WIM data source to a volume such that files can be created on the volume which are stored within the WIM.
helpviewer_keywords: ["WofWimAddEntry","WofWimAddEntry function [Files]","fs.wofwimaddentry","wofapi/WofWimAddEntry"]
old-location: fs\wofwimaddentry.htm
tech.root: fs
ms.assetid: 53CE16AE-E14D-4E51-87E2-DDF88D5CE806
ms.date: 12/05/2018
ms.keywords: WofWimAddEntry, WofWimAddEntry function [Files], fs.wofwimaddentry, wofapi/WofWimAddEntry
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
 - WofWimAddEntry
 - wofapi/WofWimAddEntry
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
 - WofWimAddEntry
---

# WofWimAddEntry function


## -description

Adds a single WIM data source to a volume such that files can be created on the volume which are stored within the WIM.

## -parameters

### -param VolumeName [in]

The path to the volume upon which files residing in the WIM should be created.

### -param WimPath [in]

The path to the WIM file which should be used to provide data to files.

### -param WimType [in]

The type of WIM. Can be <b>WIM_BOOT_OS_WIM</b> or <b>WIM_BOOT_NOT_OS_WIM</b>.

### -param WimIndex [in]

Index of the image in the WIM which is applied.

### -param DataSourceId [out]

On successful return, contains the data source used to identify the entry.  This data source can be used to create new files with <a href="/windows/desktop/api/wofapi/nf-wofapi-wofsetfiledatalocation">WofSetFileDataLocation</a>.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows-hardware/drivers/ifs/fsctl-add-overlay">FSCTL_ADD_OVERLAY</a>