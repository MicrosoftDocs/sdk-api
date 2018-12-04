---
UID: NE:dwrite_3.DWRITE_LOCALITY
title: DWRITE_LOCALITY
author: windows-sdk-content
description: Specifies the location of a resource.
old-location: directwrite\dwrite_locality.htm
tech.root: DirectWrite
ms.assetid: DEBFE4E0-C995-4468-9702-44EA37F1BCFF
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: DWRITE_LOCALITY, DWRITE_LOCALITY enumeration [Direct Write], DWRITE_LOCALITY_LOCAL, DWRITE_LOCALITY_PARTIAL, DWRITE_LOCALITY_REMOTE, directwrite.dwrite_locality, dwrite_3/DWRITE_LOCALITY, dwrite_3/DWRITE_LOCALITY_LOCAL, dwrite_3/DWRITE_LOCALITY_PARTIAL, dwrite_3/DWRITE_LOCALITY_REMOTE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - dwrite_3.h
api_name:
 - DWRITE_LOCALITY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DWRITE_LOCALITY enumeration


## -description


Specifies the location of a resource.


## -enum-fields




### -field DWRITE_LOCALITY_REMOTE

The resource is remote, and information about it is unknown, including the file size and date. If you attempt to create a font or file stream, the creation will fail until locality becomes at least partial. 


### -field DWRITE_LOCALITY_PARTIAL

The resource is partially local, which means you can query the size and date of the file stream. With this type, you also might be able to create a font face and retrieve the particular glyphs for metrics and drawing, but not all the glyphs will be present.


### -field DWRITE_LOCALITY_LOCAL

The resource is completely local, and all font functions can be called without concern of missing data or errors related to network connectivity.

