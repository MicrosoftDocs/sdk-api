---
UID: NF:winnt.IsReparseTagNameSurrogate
title: IsReparseTagNameSurrogate macro (winnt.h)
description: Determines whether a tag's associated reparse point is a surrogate for another named entity (for example, a mounted folder).
helpviewer_keywords: ["IsReparseTagNameSurrogate","IsReparseTagNameSurrogate macro [Files]","_win32_isreparsetagnamesurrogate","base.isreparsetagnamesurrogate","fs.isreparsetagnamesurrogate","winnt/IsReparseTagNameSurrogate"]
old-location: fs\isreparsetagnamesurrogate.htm
tech.root: fs
ms.assetid: 6d79527a-0c78-42d2-b079-3eb487de295f
ms.date: 12/05/2018
ms.keywords: IsReparseTagNameSurrogate, IsReparseTagNameSurrogate macro [Files], _win32_isreparsetagnamesurrogate, base.isreparsetagnamesurrogate, fs.isreparsetagnamesurrogate, winnt/IsReparseTagNameSurrogate
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
 - IsReparseTagNameSurrogate
 - winnt/IsReparseTagNameSurrogate
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
 - IsReparseTagNameSurrogate
---

# IsReparseTagNameSurrogate macro


## -description

Determines whether a tag's associated reparse point is a surrogate for another named entity (for example, a mounted folder).

## -parameters

### -param _tag

The reparse point tag to be tested for surrogacy.

## -remarks

If the surrogacy bit is set, the file or directory represents another named entity in the system, such as a mounted folder that associates this directory with another volume. For more information on volume mounting, see 
<a href="/windows/desktop/FileIO/volume-mount-points">Mounted Folders</a>.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point">FSCTL_GET_REPARSE_POINT</a>



<a href="/windows/desktop/FileIO/reparse-points">Reparse Points</a>