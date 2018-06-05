---
UID: NS:ocidl.tagAspectInfo
title: tagAspectInfo
author: windows-sdk-content
description: Contains information that is used by the IViewObject::Draw method to optimize rendering of an inactive object by making more efficient use of the GDI.
old-location: com\dvaspectinfo.htm
old-project: com
ms.assetid: c9375b9d-c822-4322-ba6f-967792257672
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: DVASPECTINFO, DVASPECTINFO structure [COM], _ole_DVASPECTINFO, com.dvaspectinfo, ocidl/DVASPECTINFO, tagAspectInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DVASPECTINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	OCIdl.h
api_name:
-	DVASPECTINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagAspectInfo structure


## -description


Contains information that is used by the <a href="https://msdn.microsoft.com/913593ff-07fe-44bd-88dc-8e58da82089b">IViewObject::Draw</a> method to optimize rendering of an inactive object by making more efficient use of the GDI.


## -struct-fields




### -field cb

The size of the structure, in bytes.


### -field dwFlags

A value taken from the <a href="https://msdn.microsoft.com/639871a6-85ab-41e2-92fa-7f1e72e9cb38">DVASPECTINFOFLAG</a> enumeration.



## -see-also




<a href="https://msdn.microsoft.com/639871a6-85ab-41e2-92fa-7f1e72e9cb38">DVASPECTINFOFLAG</a>



<a href="https://msdn.microsoft.com/913593ff-07fe-44bd-88dc-8e58da82089b">IViewObject::Draw</a>
 

 

