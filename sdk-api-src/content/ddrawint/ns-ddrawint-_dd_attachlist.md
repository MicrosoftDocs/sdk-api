---
UID: NS:ddrawint._DD_ATTACHLIST
title: "_DD_ATTACHLIST"
author: windows-sdk-content
description: The DD_ATTACHLIST structure maintains a list of attached surfaces for Microsoft DirectDraw.
old-location: display\dd_attachlist.htm
old-project: display
ms.assetid: d79b9277-ef71-4ef8-804c-d5bc8f772d0f
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: "*PDD_ATTACHLIST, DD_ATTACHLIST, DD_ATTACHLIST structure [Display Devices], _DD_ATTACHLIST, ddrawint/DD_ATTACHLIST, ddstrcts_3c38acaf-5568-4af1-ae84-a6f4752b2a02.xml, display.dd_attachlist"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: "*PDD_ATTACHLIST, DD_ATTACHLIST"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_ATTACHLIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DD_ATTACHLIST structure


## -description


The DD_ATTACHLIST structure maintains a list of attached surfaces for Microsoft DirectDraw.


## -struct-fields




### -field lpLink

Points to the next attached surface. 


### -field lpAttached

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551733">DD_SURFACE_LOCAL</a> structure that contains the attached surface local object.

