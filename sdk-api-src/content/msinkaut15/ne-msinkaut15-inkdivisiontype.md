---
UID: NE:msinkaut15.InkDivisionType
title: InkDivisionType (msinkaut15.h)
description: Defines values for the structural types within the IInkDivisionResult object.
helpviewer_keywords: ["00e1188e-58c0-4681-ad04-e53079d478fd","IDT_Drawing","IDT_Line","IDT_Paragraph","IDT_Segment","InkDivisionType","InkDivisionType enumeration [Tablet PC]","enumeration [Tablet PC]","msinkaut15/IDT_Drawing","msinkaut15/IDT_Line","msinkaut15/IDT_Paragraph","msinkaut15/IDT_Segment","msinkaut15/InkDivisionType","tablet.inkdivisiontype"]
old-location: tablet\inkdivisiontype.htm
tech.root: tablet
ms.assetid: 00e1188e-58c0-4681-ad04-e53079d478fd
ms.date: 12/05/2018
ms.keywords: 00e1188e-58c0-4681-ad04-e53079d478fd, IDT_Drawing, IDT_Line, IDT_Paragraph, IDT_Segment, InkDivisionType, InkDivisionType enumeration [Tablet PC], enumeration [Tablet PC], msinkaut15/IDT_Drawing, msinkaut15/IDT_Line, msinkaut15/IDT_Paragraph, msinkaut15/IDT_Segment, msinkaut15/InkDivisionType, tablet.inkdivisiontype
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
targetos: Windows
req.typenames: InkDivisionType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InkDivisionType
 - msinkaut15/InkDivisionType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msinkaut15.h
api_name:
 - InkDivisionType
---

# InkDivisionType enumeration


## -description

Defines values for the structural types within the <a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult">IInkDivisionResult</a> object.

## -enum-fields

### -field IDT_Segment:0

A recognition segment.

### -field IDT_Line:1

A line of handwriting that contains one or more recognition segments.

### -field IDT_Paragraph:2

A block of strokes that contains one or more lines of handwriting.

### -field IDT_Drawing:3

Ink that is not text.

## -see-also

<a href="/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_divisiontype">DivisionType Property</a>



<a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult">IInkDivisionResult Interface</a>



<a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit">IInkDivisionUnit Interface</a>



<a href="/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype">ResultByType Method</a>
