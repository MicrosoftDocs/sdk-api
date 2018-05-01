---
UID: NS:usp10.tag_SCRIPT_ITEM
title: tag_SCRIPT_ITEM
author: windows-driver-content
description: Contains a script item, including a SCRIPT_ANALYSIS structure with the string offset of the first character of the item.
old-location: intl\script_item.htm
old-project: Intl
ms.assetid: d309f3a7-fec3-4999-bbbe-bb85ceecb4c4
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: SCRIPT_ITEM, SCRIPT_ITEM structure [Internationalization for Windows Applications], _win32_SCRIPT_ITEM_str, intl.script_item, tag_SCRIPT_ITEM, usp10/SCRIPT_ITEM
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: usp10.h
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
req.typenames: SCRIPT_ITEM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Usp10.h
api_name:
-	SCRIPT_ITEM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# tag_SCRIPT_ITEM structure


## -description



Contains a script item, including a <a href="https://msdn.microsoft.com/c673d5cc-c4ca-4238-8090-55abe3db324b">SCRIPT_ANALYSIS</a> structure with the string offset of the first character of the item.




## -struct-fields




### -field iCharPos

Offset from the beginning of the itemized string to the first character of the item, counted in Unicode code points (WCHAR values).


### -field a

A <a href="https://msdn.microsoft.com/c673d5cc-c4ca-4238-8090-55abe3db324b">SCRIPT_ANALYSIS</a> structure containing the analysis of the item.


## -see-also




<a href="https://msdn.microsoft.com/c673d5cc-c4ca-4238-8090-55abe3db324b">SCRIPT_ANALYSIS</a>



<a href="https://msdn.microsoft.com/1491d9c5-e86b-45cc-bb47-85c8619eab69">ScriptItemize</a>



<a href="https://msdn.microsoft.com/da15d6b3-6725-43b8-9a2c-c19269a79d1e">ScriptItemizeOpenType</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/243438fd-5bb2-4b2a-8b33-803029085adb">Uniscribe Structures</a>
 

 

