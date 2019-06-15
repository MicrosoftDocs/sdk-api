---
UID: NF:ole2.OleCreateMenuDescriptor
title: OleCreateMenuDescriptor function (ole2.h)
author: windows-sdk-content
description: Creates and returns an OLE menu descriptor (that is, an OLE-provided data structure that describes the menus) for OLE to use when dispatching menu messages and commands.
old-location: com\olecreatemenudescriptor.htm
tech.root: com
ms.assetid: b4a6b3f1-aee9-4b68-8ffe-24bd497db0a0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: OleCreateMenuDescriptor, OleCreateMenuDescriptor function [COM], _ole_OleCreateMenuDescriptor, com.olecreatemenudescriptor, ole2/OleCreateMenuDescriptor
ms.topic: function
req.header: ole2.h
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - Ext-MS-Win-Com-OLE32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - OleCreateMenuDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# OleCreateMenuDescriptor function


## -description


Creates and returns an OLE menu descriptor (that is, an OLE-provided data structure that describes the menus) for OLE to use when dispatching menu messages and commands.


## -parameters




### -param hmenuCombined [in]

Handle to the combined menu created by the object.


### -param lpMenuWidths [in]

Pointer to an array of six <b>LONG</b> values giving the number of menus in each group.


## -returns



Returns the handle to the descriptor, or <b>NULL</b> if insufficient memory is available.





## -remarks



The <b>OleCreateMenuDescriptor</b> function can be called by the object to create a descriptor for the composite menu. OLE then uses this descriptor to dispatch menu messages and commands. To free the shared menu descriptor when it is no longer needed, the container should call the companion helper function, <a href="https://docs.microsoft.com/windows/desktop/api/ole2/nf-ole2-oledestroymenudescriptor">OleDestroyMenuDescriptor</a>.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ole2/nf-ole2-oledestroymenudescriptor">OleDestroyMenuDescriptor</a>
 

 

