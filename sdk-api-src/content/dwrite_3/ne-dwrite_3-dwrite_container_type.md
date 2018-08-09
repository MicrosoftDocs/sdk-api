---
UID: NE:dwrite_3.DWRITE_CONTAINER_TYPE
title: DWRITE_CONTAINER_TYPE
author: windows-sdk-content
description: Specifies the container format of a font resource. A container format is distinct from a font file format (DWRITE_FONT_FILE_TYPE) because the container describes the container in which the underlying font file is packaged.
old-location: directwrite\dwrite_container_type.htm
old-project: DirectWrite
ms.assetid: 93275F1D-A25C-4BDD-B278-DA56ADB3436D
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: DWRITE_CONTAINER_TYPE, DWRITE_CONTAINER_TYPE enumeration [Direct Write], DWRITE_CONTAINER_TYPE_UNKNOWN, DWRITE_CONTAINER_TYPE_WOFF, DWRITE_CONTAINER_TYPE_WOFF2, directwrite.dwrite_container_type, dwrite_3/DWRITE_CONTAINER_TYPE, dwrite_3/DWRITE_CONTAINER_TYPE_UNKNOWN, dwrite_3/DWRITE_CONTAINER_TYPE_WOFF, dwrite_3/DWRITE_CONTAINER_TYPE_WOFF2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: dwrite_3.h
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite_3.h
api_name:
 - DWRITE_CONTAINER_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DWRITE_CONTAINER_TYPE enumeration


## -description


Specifies the container format of a font resource. A container format is distinct from
          a font file format (DWRITE_FONT_FILE_TYPE) because the container describes the container
          in which the underlying font file is packaged.
        


## -enum-fields




### -field DWRITE_CONTAINER_TYPE_UNKNOWN


### -field DWRITE_CONTAINER_TYPE_WOFF


### -field DWRITE_CONTAINER_TYPE_WOFF2


## -remarks



DWRITE_CONTAINER_TYPE is returned by <a href="https://msdn.microsoft.com/A13656C9-E793-40E2-81BD-0F9C0F437F1E">IDWriteFactory5::AnalyzeContainerType</a>




