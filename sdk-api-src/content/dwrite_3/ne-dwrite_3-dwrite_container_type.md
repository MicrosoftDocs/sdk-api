---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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




