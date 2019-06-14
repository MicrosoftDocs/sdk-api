---
UID: NS:ocidl.tagAspectInfo
title: DVASPECTINFO (ocidl.h)
author: windows-sdk-content
description: Contains information that is used by the IViewObject::Draw method to optimize rendering of an inactive object by making more efficient use of the GDI.
old-location: com\dvaspectinfo.htm
tech.root: com
ms.assetid: c9375b9d-c822-4322-ba6f-967792257672
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DVASPECTINFO, DVASPECTINFO structure [COM], _ole_DVASPECTINFO, com.dvaspectinfo, ocidl/DVASPECTINFO
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
 - OCIdl.h
api_name:
 - DVASPECTINFO
product: Windows
targetos: Windows
req.typenames: DVASPECTINFO
req.redist: 
ms.custom: 19H1
---

# DVASPECTINFO structure


## -description


Contains information that is used by the <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw">IViewObject::Draw</a> method to optimize rendering of an inactive object by making more efficient use of the GDI.


## -struct-fields




### -field cb

The size of the structure, in bytes.


### -field dwFlags

A value taken from the <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/ne-ocidl-tagaspectinfoflag">DVASPECTINFOFLAG</a> enumeration.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/ne-ocidl-tagaspectinfoflag">DVASPECTINFOFLAG</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw">IViewObject::Draw</a>
 

 

