---
UID: NE:wtypes.tagSTGMOVE
title: tagSTGMOVE
author: windows-sdk-content
description: Indicate whether a storage element is to be moved or copied.
old-location: stg\stgmove.htm
old-project: Stg
ms.assetid: f55c376b-f150-406a-b960-f096c2deeff1
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: STGMOVE, STGMOVE enumeration [Structured Storage], STGMOVE_COPY, STGMOVE_MOVE, STGMOVE_SHALLOWCOPY, _stg_stgmove, stg.stgmove, tagSTGMOVE, wtypes/STGMOVE, wtypes/STGMOVE_COPY, wtypes/STGMOVE_MOVE, wtypes/STGMOVE_SHALLOWCOPY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: STGMOVE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WTypes.h
api_name:
 - STGMOVE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagSTGMOVE enumeration


## -description



			The 
<b>STGMOVE</b> enumeration values indicate whether a storage element is to be moved or copied. They are used in the 
<a href="https://msdn.microsoft.com/d9d33c64-edac-480f-b295-b2a06e51af2e">IStorage::MoveElementTo</a> method.


## -enum-fields




### -field STGMOVE_MOVE

Indicates that the method should move the data from the source to the destination.


### -field STGMOVE_COPY

Indicates that the method should copy the data from the source to the destination. A copy is the same as a move except that the source element is not removed after copying the element to the destination. Copying an element on top of itself is undefined.


### -field STGMOVE_SHALLOWCOPY

Not implemented.


## -see-also




<a href="https://msdn.microsoft.com/d9d33c64-edac-480f-b295-b2a06e51af2e">IStorage::MoveElementTo</a>
 

 

