---
UID: NF:ole2.OleCreateMenuDescriptor
title: OleCreateMenuDescriptor function
author: windows-sdk-content
description: Creates and returns an OLE menu descriptor (that is, an OLE-provided data structure that describes the menus) for OLE to use when dispatching menu messages and commands.
old-location: com\olecreatemenudescriptor.htm
old-project: com
ms.assetid: b4a6b3f1-aee9-4b68-8ffe-24bd497db0a0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: OleCreateMenuDescriptor, OleCreateMenuDescriptor function [COM], _ole_OleCreateMenuDescriptor, com.olecreatemenudescriptor, ole2/OleCreateMenuDescriptor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ole2.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: QACONTROL
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
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



The <b>OleCreateMenuDescriptor</b> function can be called by the object to create a descriptor for the composite menu. OLE then uses this descriptor to dispatch menu messages and commands. To free the shared menu descriptor when it is no longer needed, the container should call the companion helper function, <a href="https://msdn.microsoft.com/dc347d39-a7bb-4bbf-8957-c3fbcff461bf">OleDestroyMenuDescriptor</a>.





## -see-also




<a href="https://msdn.microsoft.com/dc347d39-a7bb-4bbf-8957-c3fbcff461bf">OleDestroyMenuDescriptor</a>
 

 

