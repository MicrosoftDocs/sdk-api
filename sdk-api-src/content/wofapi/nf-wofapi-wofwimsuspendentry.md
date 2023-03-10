---
UID: NF:wofapi.WofWimSuspendEntry
title: WofWimSuspendEntry function (wofapi.h)
description: Temporarily removes a WIM data source from backing files on a volume until the volume is remounted or the data source is updated with WofWimUpdateEntry.
helpviewer_keywords: ["WofWimSuspendEntry","WofWimSuspendEntry function [Files]","fs.wofwimsuspendentry","wofapi/WofWimSuspendEntry"]
old-location: fs\wofwimsuspendentry.htm
tech.root: fs
ms.assetid: 1F3DA0FF-37B5-4DEE-BEA0-7A0E63F3E97D
ms.date: 12/05/2018
ms.keywords: WofWimSuspendEntry, WofWimSuspendEntry function [Files], fs.wofwimsuspendentry, wofapi/WofWimSuspendEntry
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
 - WofWimSuspendEntry
 - wofapi/WofWimSuspendEntry
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
 - WofWimSuspendEntry
---

# WofWimSuspendEntry function


## -description

Temporarily removes a WIM data source from backing files on a volume until the volume is remounted or the data source is updated with <a href="/windows/desktop/api/wofapi/nf-wofapi-wofwimupdateentry">WofWimUpdateEntry</a>.

## -parameters

### -param VolumeName [in]

The volume name which contained files whose data was provided by the WIM.

### -param DataSourceId [in]

Identifies the WIM entry.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the volume currently has files whose data is derived from the WIM file, the data for those files will become temporarily inaccessible. This should not be performed on a WIM from which the system is currently operating.

## -see-also

<a href="/windows-hardware/drivers/ifs/fsctl-suspend-overlay">FSCTL_SUSPEND_OVERLAY</a>