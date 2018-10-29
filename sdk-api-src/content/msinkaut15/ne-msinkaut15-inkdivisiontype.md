---
UID: NE:msinkaut15.InkDivisionType
title: InkDivisionType
author: windows-sdk-content
description: Defines values for the structural types within the IInkDivisionResult object.
old-location: tablet\inkdivisiontype.htm
tech.root: tablet
ms.assetid: 00e1188e-58c0-4681-ad04-e53079d478fd
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 00e1188e-58c0-4681-ad04-e53079d478fd, IDT_Drawing, IDT_Line, IDT_Paragraph, IDT_Segment, InkDivisionType, InkDivisionType enumeration [Tablet PC], enumeration [Tablet PC], msinkaut15/IDT_Drawing, msinkaut15/IDT_Line, msinkaut15/IDT_Paragraph, msinkaut15/IDT_Segment, msinkaut15/InkDivisionType, tablet.inkdivisiontype
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: msinkaut15.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
 - msinkaut15.h
api_name:
 - InkDivisionType
product: Windows
targetos: Windows
req.typenames: InkDivisionType
req.redist: 
---

# InkDivisionType enumeration


## -description



Defines values for the structural types within the <a href="https://msdn.microsoft.com/d1a71976-2825-48d2-812c-fd2336cd4c1d">IInkDivisionResult</a> object.




## -enum-fields




### -field IDT_Segment

A recognition segment.


### -field IDT_Line

A line of handwriting that contains one or more recognition segments.


### -field IDT_Paragraph

A block of strokes that contains one or more lines of handwriting.


### -field IDT_Drawing

Ink that is not text.


## -see-also




<a href="https://msdn.microsoft.com/c1aaaa62-34fc-4cd4-bd68-47f828bb59b1">DivisionType Property</a>



<a href="https://msdn.microsoft.com/d1a71976-2825-48d2-812c-fd2336cd4c1d">IInkDivisionResult Interface</a>



<a href="https://msdn.microsoft.com/5c5479e0-7568-40c8-bb75-e2ded3ac86b7">IInkDivisionUnit Interface</a>



<a href="https://msdn.microsoft.com/d0bad0e8-e48c-443b-b52e-e95de3158710">ResultByType Method</a>
 

 

