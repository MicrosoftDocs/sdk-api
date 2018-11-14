---
UID: NS:ocidl.tagExtentInfo
title: tagExtentInfo
author: windows-sdk-content
description: Represents the sizing data used in IViewObjectEx::GetNaturalExtent.
old-location: com\dvextentinfo.htm
tech.root: com
ms.assetid: bd603de2-39db-43a1-a391-01dcfedc073f
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DVEXTENTINFO, DVEXTENTINFO structure [COM], _ole_DVEXTENTINFO, com.dvextentinfo, ocidl/DVEXTENTINFO, tagExtentInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - OCIdl.h
api_name:
 - DVEXTENTINFO
product: Windows
targetos: Windows
req.typenames: DVEXTENTINFO
req.redist: 
---

# tagExtentInfo structure


## -description


Represents the sizing data used in <a href="https://msdn.microsoft.com/5759c482-2dea-4b94-956d-9560f72acbd5">IViewObjectEx::GetNaturalExtent</a>.


## -struct-fields




### -field cb

The size of the structure, in bytes.


### -field dwExtentMode

Indicates whether the sizing mode is content or integral sizing. See the <a href="https://msdn.microsoft.com/5848c26d-d185-4ad9-8841-bb8b622364ee">DVEXTENTMODE</a> enumeration for possible values.


### -field sizelProposed

The proposed size in content sizing or the preferred size in integral sizing.


## -see-also




<a href="https://msdn.microsoft.com/5848c26d-d185-4ad9-8841-bb8b622364ee">DVEXTENTMODE</a>



<a href="https://msdn.microsoft.com/5759c482-2dea-4b94-956d-9560f72acbd5">IViewObjectEx::GetNaturalExtent</a>
 

 

