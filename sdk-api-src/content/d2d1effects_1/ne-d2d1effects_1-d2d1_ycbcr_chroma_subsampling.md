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

# D2D1_YCBCR_CHROMA_SUBSAMPLING enumeration


## -description



          Specifies the chroma subsampling of the input chroma image used by the <a href="https://msdn.microsoft.com/E4492996-54DA-4C5F-B44C-8FBE97C8DD7D">YCbCr effect</a>.
        


## -enum-fields




### -field D2D1_YCBCR_CHROMA_SUBSAMPLING_AUTO

This mode attempts to infer the chroma subsampling from the bounds of the input images. When this option is selected, 
          the smaller plane is upsampled to the size of the larger plane and this effect’s output rectangle is the intersection of the two planes. 
          When using this mode, care should be taken when applying effects to the input planes that change the image bounds, such as the border transform, 
          so that the desired size ratio between the planes is maintained.


### -field D2D1_YCBCR_CHROMA_SUBSAMPLING_420

The chroma plane is horizontally subsampled by 1/2 and vertically subsampled by 1/2. 
          When this option is selected, the chroma plane is horizontally and vertically upsampled by 2x and this effect's output rectangle is the intersection of the two planes.


### -field D2D1_YCBCR_CHROMA_SUBSAMPLING_422

The chroma plane is horizontally subsampled by 1/2. When this option is selected, 
          the chroma plane is horizontally upsampled by 2x and this effect's output rectangle is the intersection of the two planes.


### -field D2D1_YCBCR_CHROMA_SUBSAMPLING_444

The chroma plane is not subsampled. When this option is selected this effect’s output rectangle is the intersection of the two planes.


### -field D2D1_YCBCR_CHROMA_SUBSAMPLING_440

The chroma plane is vertically subsampled by 1/2. When this option is selected, the chroma plane is vertically upsampled by 2x and this effect's 
          output rectangle is the intersection of the two planes.


### -field D2D1_YCBCR_CHROMA_SUBSAMPLING_FORCE_DWORD



