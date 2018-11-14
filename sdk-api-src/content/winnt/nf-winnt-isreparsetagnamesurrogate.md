---
UID: NF:winnt.IsReparseTagNameSurrogate
title: IsReparseTagNameSurrogate macro
author: windows-sdk-content
description: Determines whether a tag's associated reparse point is a surrogate for another named entity (for example, a mounted folder).
old-location: fs\isreparsetagnamesurrogate.htm
tech.root: fileio
ms.assetid: 6d79527a-0c78-42d2-b079-3eb487de295f
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IsReparseTagNameSurrogate, IsReparseTagNameSurrogate macro [Files], _win32_isreparsetagnamesurrogate, base.isreparsetagnamesurrogate, fs.isreparsetagnamesurrogate, winnt/IsReparseTagNameSurrogate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - IsReparseTagNameSurrogate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- winnt.h
: 
- IsReparseTagNameSurrogate
: 
---

# IsReparseTagNameSurrogate macro


## -description


Determines whether a tag's associated reparse point is a surrogate for another named entity (for example, a mounted folder).


## -parameters




### -param _tag

The reparse point tag to be tested for surrogacy.


## -remarks



If the surrogacy bit is set, the file or directory represents another named entity in the system, such as a mounted folder that associates this directory with another volume. For more information on volume mounting, see 
<a href="https://msdn.microsoft.com/6de526cd-5537-4411-b43f-3c0bdac70d64">Mounted Folders</a>.




## -see-also




<a href="https://msdn.microsoft.com/6f1b7ea2-aed6-4ab4-8e92-1b77ab5cfefb">FSCTL_GET_REPARSE_POINT</a>



<a href="https://msdn.microsoft.com/3abb3a08-9a00-43eb-9792-82eab1a25f06">Reparse Points</a>
 

 

