---
UID: NE:ctffunc.__MIDL_ITfFnGetPreferredTouchKeyboardLayout_0001
title: TKBLayoutType (ctffunc.h)
author: windows-sdk-content
description: Elements of the TKBLayoutType enumeration are passed by an IME in a call to ITfFnGetPreferredTouchKeyboardLayout::GetLayout to specify the type of layout.
old-location: tsf\tkblayouttype.htm
tech.root: TSF
ms.assetid: 65C46775-9D4D-4C80-A5F0-6713C805053D
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TKBLT_CLASSIC, TKBLT_OPTIMIZED, TKBLT_UNDEFINED, TKBLayoutType, TKBLayoutType enumeration [Text Services Framework], ctffunc/TKBLT_CLASSIC, ctffunc/TKBLT_OPTIMIZED, ctffunc/TKBLT_UNDEFINED, ctffunc/TKBLayoutType, tsf.tkblayouttype
ms.topic: enum
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
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
 - Ctffunc.h
api_name:
 - TKBLayoutType
product: Windows
targetos: Windows
req.typenames: TKBLayoutType
req.redist: 
---

# TKBLayoutType enumeration


## -description


Elements of the <b>TKBLayoutType</b> enumeration are passed by an IME in a call to <a href="https://msdn.microsoft.com/03C14744-A4A3-4C62-8E7F-CDCC638BBCA1">ITfFnGetPreferredTouchKeyboardLayout::GetLayout</a> to specify the type of layout.




## -enum-fields




### -field TKBLT_UNDEFINED

 Undefined. If specified, it will cause the layout to fallback to a classic layout.


### -field TKBLT_CLASSIC

The touch keyboard is to use a classic layout.


### -field TKBLT_OPTIMIZED

The touch keyboard is to use a touch-optimized layout.


## -see-also




<a href="https://msdn.microsoft.com/03C14744-A4A3-4C62-8E7F-CDCC638BBCA1">ITfFnGetPreferredTouchKeyboardLayout::GetLayout</a>
 

 

