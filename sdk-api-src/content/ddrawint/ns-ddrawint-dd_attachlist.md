---
UID: NS:ddrawint._DD_ATTACHLIST
title: DD_ATTACHLIST (ddrawint.h)
description: The DD_ATTACHLIST structure maintains a list of attached surfaces for Microsoft DirectDraw.
helpviewer_keywords: ["*PDD_ATTACHLIST","DD_ATTACHLIST","DD_ATTACHLIST structure [Display Devices]","ddrawint/DD_ATTACHLIST","ddstrcts_3c38acaf-5568-4af1-ae84-a6f4752b2a02.xml","display.dd_attachlist"]
old-location: display\dd_attachlist.htm
tech.root: display
ms.assetid: d79b9277-ef71-4ef8-804c-d5bc8f772d0f
ms.date: 12/05/2018
ms.keywords: '*PDD_ATTACHLIST, DD_ATTACHLIST, DD_ATTACHLIST structure [Display Devices], ddrawint/DD_ATTACHLIST, ddstrcts_3c38acaf-5568-4af1-ae84-a6f4752b2a02.xml, display.dd_attachlist'
req.header: ddrawint.h
req.include-header: Winddi.h
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
targetos: Windows
req.typenames: '*PDD_ATTACHLIST, DD_ATTACHLIST'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_ATTACHLIST
 - ddrawint/_DD_ATTACHLIST
 - PDD_ATTACHLIST
 - ddrawint/PDD_ATTACHLIST
 - DD_ATTACHLIST
 - ddrawint/DD_ATTACHLIST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_ATTACHLIST
---

# DD_ATTACHLIST structure


## -description

The DD_ATTACHLIST structure maintains a list of attached surfaces for Microsoft DirectDraw.

## -struct-fields

### -field lpLink

Points to the next attached surface.

### -field lpAttached

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure that contains the attached surface local object.