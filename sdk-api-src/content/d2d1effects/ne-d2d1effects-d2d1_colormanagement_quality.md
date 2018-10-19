---
UID: NE:d2d1effects.D2D1_COLORMANAGEMENT_QUALITY
title: D2D1_COLORMANAGEMENT_QUALITY
author: windows-sdk-content
description: The quality level of the transform for the Color management effect.
old-location: direct2d\d2d1_colormanagement_quality.htm
tech.root: direct2d
ms.assetid: 99BB95AE-E5C6-4D56-9EB9-740DD7D0EFEF
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: D2D1_COLORMANAGEMENT_QUALITY, D2D1_COLORMANAGEMENT_QUALITY enumeration [Direct2D], D2D1_COLORMANAGEMENT_QUALITY_BEST, D2D1_COLORMANAGEMENT_QUALITY_NORMAL, D2D1_COLORMANAGEMENT_QUALITY_PROOF, d2d1effects/D2D1_COLORMANAGEMENT_QUALITY, d2d1effects/D2D1_COLORMANAGEMENT_QUALITY_BEST, d2d1effects/D2D1_COLORMANAGEMENT_QUALITY_NORMAL, d2d1effects/D2D1_COLORMANAGEMENT_QUALITY_PROOF, direct2d.d2d1_colormanagement_quality
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1effects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - d2d1effects.h
api_name:
 - D2D1_COLORMANAGEMENT_QUALITY
product: Windows
targetos: Windows
req.typenames: D2D1_COLORMANAGEMENT_QUALITY
req.redist: 
---

# D2D1_COLORMANAGEMENT_QUALITY enumeration


## -description


The quality level of the transform for the <a href="https://msdn.microsoft.com/7351C4B4-F289-4236-BB42-1B3BD8753248">Color management effect</a>. 


## -enum-fields




### -field D2D1_COLORMANAGEMENT_QUALITY_PROOF

The lowest quality mode. This mode requires feature level 9_1 or above.


### -field D2D1_COLORMANAGEMENT_QUALITY_NORMAL

Normal quality mode. This mode requires feature level 9_1 or above.


### -field D2D1_COLORMANAGEMENT_QUALITY_BEST

The best quality mode. This mode requires feature level 10_0 or above, as well as floating point precision buffers. 
          This mode supports floating point precision as well as extended range as defined in the ICC v4.3 specification. 


### -field D2D1_COLORMANAGEMENT_QUALITY_FORCE_DWORD



