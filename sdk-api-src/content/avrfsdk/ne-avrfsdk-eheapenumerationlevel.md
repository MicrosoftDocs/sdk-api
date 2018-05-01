---
UID: NE:avrfsdk.eHeapEnumerationLevel
title: eHeapEnumerationLevel
author: windows-driver-content
description: Determines whether the enumeration operation should continue or stop.
old-location: winprog\eheapenumerationlevel.htm
old-project: DevNotes
ms.assetid: f8260ae8-eb1e-45f4-babc-905f4af7e3b1
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: HeapEnumerationEverything, HeapEnumerationStop, avrfsdk/HeapEnumerationEverything, avrfsdk/HeapEnumerationStop, avrfsdk/eHeapEnumerationLevel, base.eheapenumerationlevel, eHeapEnumerationLevel, eHeapEnumerationLevel enumeration [Windows API], winprog.eheapenumerationlevel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: avrfsdk.h
req.include-header: 
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Avrfsdk.h
api_name:
-	eHeapEnumerationLevel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# eHeapEnumerationLevel enumeration


## -description


Determines whether the enumeration operation should continue or stop.


## -enum-fields




### -field HeapEnumerationEverything

A constant that specifies the enumeration should continue.


### -field HeapEnumerationStop

A constant that specifies to the <a href="https://msdn.microsoft.com/e1715f2a-5928-44e6-afbf-f2f0ab0ba3dd">VerifierEnumerateResource</a> function when the enumeration operation should stop.

Codes from 0x1 to 0xFFFFFFE are reserved.


## -see-also




<a href="https://msdn.microsoft.com/99cb9005-9cfc-44fb-b09f-fed0541cda37">Resource Enumeration</a>



<a href="https://msdn.microsoft.com/e1715f2a-5928-44e6-afbf-f2f0ab0ba3dd">VerifierEnumerateResource</a>
 

 

