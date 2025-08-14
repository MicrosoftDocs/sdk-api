---
UID: NF:ole2.OleDestroyMenuDescriptor
title: OleDestroyMenuDescriptor function (ole2.h)
description: Called by the container to free the shared menu descriptor allocated by the OleCreateMenuDescriptor function.
helpviewer_keywords: ["OleDestroyMenuDescriptor","OleDestroyMenuDescriptor function [COM]","_ole_OleDestroyMenuDescriptor","com.oledestroymenudescriptor","ole2/OleDestroyMenuDescriptor"]
old-location: com\oledestroymenudescriptor.htm
tech.root: com
ms.assetid: dc347d39-a7bb-4bbf-8957-c3fbcff461bf
ms.date: 12/05/2018
ms.keywords: OleDestroyMenuDescriptor, OleDestroyMenuDescriptor function [COM], _ole_OleDestroyMenuDescriptor, com.oledestroymenudescriptor, ole2/OleDestroyMenuDescriptor
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleDestroyMenuDescriptor
 - ole2/OleDestroyMenuDescriptor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - ext-ms-win-com-ole32-l1-1-5.dll
 - Ole32.dll
 - Ext-MS-Win-Com-OLE32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - OleDestroyMenuDescriptor
req.apiset: ext-ms-win-com-ole32-l1-1-3 (introduced in Windows 10, version 10.0.10240)
---

# OleDestroyMenuDescriptor function


## -description

Called by the container to free the shared menu descriptor allocated by the <a href="/windows/desktop/api/ole2/nf-ole2-olecreatemenudescriptor">OleCreateMenuDescriptor</a> function.

## -parameters

### -param holemenu [in]

Handle to the shared menu descriptor that was returned by the <a href="/windows/desktop/api/ole2/nf-ole2-olecreatemenudescriptor">OleCreateMenuDescriptor</a> function.

## -returns

This function does not return a value.

## -see-also

<a href="/windows/desktop/api/ole2/nf-ole2-olecreatemenudescriptor">OleCreateMenuDescriptor</a>
