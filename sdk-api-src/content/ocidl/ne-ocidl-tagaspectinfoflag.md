---
UID: NE:ocidl.tagAspectInfoFlag
title: tagAspectInfoFlag
author: windows-sdk-content
description: Indicates whether an object can support optimized drawing of itself.
old-location: com\dvaspectinfoflag.htm
old-project: com
ms.assetid: 639871a6-85ab-41e2-92fa-7f1e72e9cb38
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: DVASPECTINFOFLAG, DVASPECTINFOFLAG enumeration [COM], DVASPECTINFOFLAG_CANOPTIMIZE, _ole_DVASPECTINFOFLAG, com.dvaspectinfoflag, ocidl/DVASPECTINFOFLAG, ocidl/DVASPECTINFOFLAG_CANOPTIMIZE, tagAspectInfoFlag
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: ocidl.h
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
req.typenames: DVASPECTINFOFLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	OCIdl.h
api_name:
-	DVASPECTINFOFLAG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagAspectInfoFlag enumeration


## -description


Indicates whether an object can support optimized drawing of itself.


## -enum-fields




### -field DVASPECTINFOFLAG_CANOPTIMIZE

Indicates that the object can support optimized rendering of itself. Because most objects on a form share the same font, background color, and border types, leaving these values in the device context allows the next object to use them without having to re-select them. Specifically, the object can leave the font, brush, and pen selected on return from the <a href="https://msdn.microsoft.com/913593ff-07fe-44bd-88dc-8e58da82089b">IViewObject::Draw</a> method instead of deselecting these from the device context. The container then must deselect these values at the end of the overall drawing process. The object can also leave other drawing state changes in the device context, such as the background color, the text color, raster operation code, the current point, the line drawing, and the poly fill mode. The object cannot change state values unless other objects are capable of restoring them. For example, the object cannot leave a changed mode, transformation value, selected bitmap, clip region, or metafile.


## -see-also




<a href="https://msdn.microsoft.com/c9375b9d-c822-4322-ba6f-967792257672">DVASPECTINFO</a>
 

 

