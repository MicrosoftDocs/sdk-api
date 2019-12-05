---
UID: NE:ocidl.tagACTIVATEFLAGS
title: ACTIVATEFLAGS (ocidl.h)
description: Indicates whether an object is activated as a windowless object. It is used in IOleInPlaceSiteEx::OnInPlaceActivateEx.
old-location: com\activateflags.htm
tech.root: com
ms.assetid: 8748d3aa-3fea-4705-959c-3bc86b13a868
ms.date: 12/05/2018
ms.keywords: ACTIVATEFLAGS, ACTIVATEFLAGS enumeration [COM], ACTIVATE_WINDOWLESS, _ole_ACTIVATEFLAGS, com.activateflags, ocidl/ACTIVATEFLAGS, ocidl/ACTIVATE_WINDOWLESS
ms.topic: enum
f1_keywords:
- ocidl/ACTIVATEFLAGS
dev_langs:
- c++
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
- ACTIVATEFLAGS
targetos: Windows
req.typenames: ACTIVATEFLAGS
req.redist: 
ms.custom: 19H1
---

# ACTIVATEFLAGS enumeration


## -description


Indicates whether an object is activated as a windowless object. It is used in <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesiteex">IOleInPlaceSiteEx::OnInPlaceActivateEx</a>.




## -enum-fields




### -field ACTIVATE_WINDOWLESS

 Indicates that the object is activated in place as a windowless object. In the <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesiteex">IOleInPlaceSiteEx::OnInPlaceActivateEx</a> method, the container uses this value returned in the <i>dwFlags</i> parameter instead of calling the <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ioleinplaceobjectwindowless">IOleInPlaceObjectWindowless::GetWindow</a>  method to determine if the object is windowless or not.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesiteex">IOleInPlaceSiteEx::OnInPlaceActivateEx</a>
 

 

