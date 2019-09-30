---
UID: NF:ole2.OleDestroyMenuDescriptor
title: OleDestroyMenuDescriptor function (ole2.h)
author: windows-sdk-content
description: Called by the container to free the shared menu descriptor allocated by the OleCreateMenuDescriptor function.
old-location: com\oledestroymenudescriptor.htm
tech.root: com
ms.assetid: dc347d39-a7bb-4bbf-8957-c3fbcff461bf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: OleDestroyMenuDescriptor, OleDestroyMenuDescriptor function [COM], _ole_OleDestroyMenuDescriptor, com.oledestroymenudescriptor, ole2/OleDestroyMenuDescriptor
ms.topic: function
f1_keywords: 
 - "ole2/OleDestroyMenuDescriptor"
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
 - OleDestroyMenuDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# OleDestroyMenuDescriptor function


## -description


Called by the container to free the shared menu descriptor allocated by the <a href="https://docs.microsoft.com/windows/desktop/api/ole2/nf-ole2-olecreatemenudescriptor">OleCreateMenuDescriptor</a> function.


## -parameters




### -param holemenu [in]

Handle to the shared menu descriptor that was returned by the <a href="https://docs.microsoft.com/windows/desktop/api/ole2/nf-ole2-olecreatemenudescriptor">OleCreateMenuDescriptor</a> function.


## -returns



This function does not return a value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ole2/nf-ole2-olecreatemenudescriptor">OleCreateMenuDescriptor</a>
 

 

