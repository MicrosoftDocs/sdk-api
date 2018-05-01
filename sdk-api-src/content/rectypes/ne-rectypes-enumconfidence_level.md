---
UID: NE:rectypes.enumCONFIDENCE_LEVEL
title: enumCONFIDENCE_LEVEL
author: windows-driver-content
description: Indicates the level of confidence the recognizer has in the recognition result.
old-location: tablet\confidence_level.htm
old-project: tablet
ms.assetid: 94167a91-7d72-40c9-bce4-29babdb5bff9
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: 94167a91-7d72-40c9-bce4-29babdb5bff9, CFL_INTERMEDIATE, CFL_POOR, CFL_STRONG, CONFIDENCE_LEVEL, CONFIDENCE_LEVEL enumeration [Tablet PC], enumCONFIDENCE_LEVEL, rectypes/CFL_INTERMEDIATE, rectypes/CFL_POOR, rectypes/CFL_STRONG, rectypes/CONFIDENCE_LEVEL, tablet.confidence_level
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: CONFIDENCE_LEVEL, CONFIDENCE_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	rectypes.h
api_name:
-	CONFIDENCE_LEVEL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# enumCONFIDENCE_LEVEL enumeration


## -description



Indicates the level of confidence the recognizer has in the recognition result.




## -enum-fields




### -field CFL_STRONG

The recognizer is confident that the best alternate is correct.


### -field CFL_INTERMEDIATE

The recognizer is confident that the correct result is in the list of alternates.


### -field CFL_POOR

The recognizer is not confident that the result is in the list of alternates.

