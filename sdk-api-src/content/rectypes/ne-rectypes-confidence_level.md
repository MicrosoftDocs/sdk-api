---
UID: NE:rectypes.enumCONFIDENCE_LEVEL
title: CONFIDENCE_LEVEL (rectypes.h)
description: Indicates the level of confidence the recognizer has in the recognition result.
helpviewer_keywords: ["94167a91-7d72-40c9-bce4-29babdb5bff9","CFL_INTERMEDIATE","CFL_POOR","CFL_STRONG","CONFIDENCE_LEVEL","CONFIDENCE_LEVEL enumeration [Tablet PC]","rectypes/CFL_INTERMEDIATE","rectypes/CFL_POOR","rectypes/CFL_STRONG","rectypes/CONFIDENCE_LEVEL","tablet.confidence_level"]
old-location: tablet\confidence_level.htm
tech.root: tablet
ms.assetid: 94167a91-7d72-40c9-bce4-29babdb5bff9
ms.date: 12/05/2018
ms.keywords: 94167a91-7d72-40c9-bce4-29babdb5bff9, CFL_INTERMEDIATE, CFL_POOR, CFL_STRONG, CONFIDENCE_LEVEL, CONFIDENCE_LEVEL enumeration [Tablet PC], rectypes/CFL_INTERMEDIATE, rectypes/CFL_POOR, rectypes/CFL_STRONG, rectypes/CONFIDENCE_LEVEL, tablet.confidence_level
req.header: rectypes.h
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
req.typenames: CONFIDENCE_LEVEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - enumCONFIDENCE_LEVEL
 - rectypes/enumCONFIDENCE_LEVEL
 - CONFIDENCE_LEVEL
 - rectypes/CONFIDENCE_LEVEL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - rectypes.h
api_name:
 - CONFIDENCE_LEVEL
---

# CONFIDENCE_LEVEL enumeration


## -description

Indicates the level of confidence the recognizer has in the recognition result.

## -enum-fields

### -field CFL_STRONG:0

The recognizer is confident that the best alternate is correct.

### -field CFL_INTERMEDIATE:1

The recognizer is confident that the correct result is in the list of alternates.

### -field CFL_POOR:2

The recognizer is not confident that the result is in the list of alternates.

