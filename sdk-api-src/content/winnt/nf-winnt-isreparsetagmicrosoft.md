---
UID: NF:winnt.IsReparseTagMicrosoft
title: IsReparseTagMicrosoft macro (winnt.h)
description: Determines whether a reparse point tag indicates a Microsoft reparse point.
helpviewer_keywords: ["IsReparseTagMicrosoft","IsReparseTagMicrosoft macro [Files]","_win32_isreparsetagmicrosoft","base.isreparsetagmicrosoft","fs.isreparsetagmicrosoft","winnt/IsReparseTagMicrosoft"]
old-location: fs\isreparsetagmicrosoft.htm
tech.root: fs
ms.assetid: f64378a7-084e-41c7-9331-dcffa11e0ae9
ms.date: 07/01/2025
ms.keywords: IsReparseTagMicrosoft, IsReparseTagMicrosoft macro [Files], _win32_isreparsetagmicrosoft, base.isreparsetagmicrosoft, fs.isreparsetagmicrosoft, winnt/IsReparseTagMicrosoft
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsReparseTagMicrosoft
 - winnt/IsReparseTagMicrosoft
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - IsReparseTagMicrosoft
---

# IsReparseTagMicrosoft macro

## -syntax

```cpp
ULONG IsReparseTagMicrosoft(
    ULONG _tag
);
```

## -returns

Type: **ULONG**

A nonzero return value indicates that the tag is a Microsoft tag. A zero return value indicates that the tag is not a Microsoft tag. Only software developed by Microsoft or in partnership with Microsoft can use Microsoft tags. All other software must use non-Microsoft tags.


## -description

Determines whether a reparse point tag indicates a Microsoft reparse point.

## -parameters

### -param _tag

The reparse point tag to be tested.

## -remarks

If the Microsoft tag bit is set, Microsoft provides the tag. All other tags must use zero for this bit.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point">FSCTL_GET_REPARSE_POINT</a>



<a href="/windows/desktop/FileIO/reparse-points">Reparse Points</a>
