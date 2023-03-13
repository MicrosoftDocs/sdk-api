---
UID: NE:dwrite.DWRITE_READING_DIRECTION
title: DWRITE_READING_DIRECTION (dwrite.h)
description: Specifies the direction in which reading progresses.
helpviewer_keywords: ["DWRITE_READING_DIRECTION","DWRITE_READING_DIRECTION enumeration [Direct Write]","DWRITE_READING_DIRECTION_BOTTOM_TO_TOP","DWRITE_READING_DIRECTION_LEFT_TO_RIGHT","DWRITE_READING_DIRECTION_RIGHT_TO_LEFT","DWRITE_READING_DIRECTION_TOP_TO_BOTTOM","directwrite.dwrite_reading_direction","dwrite/DWRITE_READING_DIRECTION","dwrite/DWRITE_READING_DIRECTION_BOTTOM_TO_TOP","dwrite/DWRITE_READING_DIRECTION_LEFT_TO_RIGHT","dwrite/DWRITE_READING_DIRECTION_RIGHT_TO_LEFT","dwrite/DWRITE_READING_DIRECTION_TOP_TO_BOTTOM"]
old-location: directwrite\dwrite_reading_direction.htm
tech.root: DirectWrite
ms.assetid: 37288d34-d533-474c-b3c0-8c6361074a9b
ms.date: 12/05/2018
ms.keywords: DWRITE_READING_DIRECTION, DWRITE_READING_DIRECTION enumeration [Direct Write], DWRITE_READING_DIRECTION_BOTTOM_TO_TOP, DWRITE_READING_DIRECTION_LEFT_TO_RIGHT, DWRITE_READING_DIRECTION_RIGHT_TO_LEFT, DWRITE_READING_DIRECTION_TOP_TO_BOTTOM, directwrite.dwrite_reading_direction, dwrite/DWRITE_READING_DIRECTION, dwrite/DWRITE_READING_DIRECTION_BOTTOM_TO_TOP, dwrite/DWRITE_READING_DIRECTION_LEFT_TO_RIGHT, dwrite/DWRITE_READING_DIRECTION_RIGHT_TO_LEFT, dwrite/DWRITE_READING_DIRECTION_TOP_TO_BOTTOM
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DWRITE_READING_DIRECTION
 - dwrite/DWRITE_READING_DIRECTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite.h
api_name:
 - DWRITE_READING_DIRECTION
---

# DWRITE_READING_DIRECTION enumeration


## -description

Specifies the direction in which reading progresses.
  
<div class="alert"><b>Note</b>  <b>DWRITE_READING_DIRECTION_TOP_TO_BOTTOM</b> and <b>DWRITE_READING_DIRECTION_BOTTOM_TO_TOP</b> are available in Windows 8.1 and later, only.</div><div> </div>

## -enum-fields

### -field DWRITE_READING_DIRECTION_LEFT_TO_RIGHT:0

Indicates that reading progresses from left to right.

### -field DWRITE_READING_DIRECTION_RIGHT_TO_LEFT:1

Indicates that reading progresses from right to left.

### -field DWRITE_READING_DIRECTION_TOP_TO_BOTTOM:2

<div class="alert"><b>Note</b>  Windows 8.1 and later only.</div>
<div> </div>
Indicates that reading progresses from top to bottom.

### -field DWRITE_READING_DIRECTION_BOTTOM_TO_TOP:3

<div class="alert"><b>Note</b>  Windows 8.1 and later only.</div>
<div> </div>
 Indicates that reading progresses from bottom to top.

