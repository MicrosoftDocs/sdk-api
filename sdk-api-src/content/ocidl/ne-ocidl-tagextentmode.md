---
UID: NE:ocidl.tagExtentMode
title: tagExtentMode
author: windows-sdk-content
description: Indicates whether the sizing mode is content or integral sizing.
old-location: com\dvextentmode.htm
tech.root: com
ms.assetid: 5848c26d-d185-4ad9-8841-bb8b622364ee
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DVEXTENTMODE, DVEXTENTMODE enumeration [COM], DVEXTENT_CONTENT, DVEXTENT_INTEGRAL, _ole_DVEXTENTMODE, com.dvextentmode, ocidl/DVEXTENTMODE, ocidl/DVEXTENT_CONTENT, ocidl/DVEXTENT_INTEGRAL, tagExtentMode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - DVEXTENTMODE
product: Windows
targetos: Windows
req.typenames: DVEXTENTMODE
req.redist: 
---

# tagExtentMode enumeration


## -description


Indicates whether the sizing mode is content or integral sizing.


## -enum-fields




### -field DVEXTENT_CONTENT

Indicates that the container will ask the object how big it wants to be to exactly fit its content, for example, in snap-to-size operations.


### -field DVEXTENT_INTEGRAL

Indicates that the container will provide a proposed size to the object for its use in resizing.


## -see-also




<a href="https://msdn.microsoft.com/bd603de2-39db-43a1-a391-01dcfedc073f">DVEXTENTINFO</a>



<a href="https://msdn.microsoft.com/5759c482-2dea-4b94-956d-9560f72acbd5">IViewObjectEx::GetNaturalExtent</a>
 

 

