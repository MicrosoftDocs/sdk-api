---
UID: NS:mfobjects._MFVideoSurfaceInfo
title: "_MFVideoSurfaceInfo"
author: windows-sdk-content
description: Contains information about an uncompressed video format. This structure is used in the MFVIDEOFORMAT structure.
old-location: mf\mfvideosurfaceinfo.htm
tech.root: medfound
ms.assetid: b48099a2-8427-496c-9a60-ace5b89d81e9
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: MFVideoSurfaceInfo, MFVideoSurfaceInfo structure [Media Foundation], _MFVideoSurfaceInfo, b48099a2-8427-496c-9a60-ace5b89d81e9, mf.mfvideosurfaceinfo, mfobjects/MFVideoSurfaceInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - mfobjects.h
api_name:
 - MFVideoSurfaceInfo
product: Windows
targetos: Windows
req.typenames: MFVideoSurfaceInfo
req.redist: 
---

# _MFVideoSurfaceInfo structure


## -description



Contains information about an uncompressed video format. This structure is used in the <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a> structure.




## -struct-fields




### -field Format

For compressed formats, this value must be zero. For uncompressed formats, the value is a FOURCC or <b>D3DFORMAT</b> value that identifies the format. Use the <b>Data1</b> field from the subtype GUID. See <a href="https://msdn.microsoft.com/7dfd85e6-936e-4b78-a2cb-a5d59153e1c4">Video Subtype GUIDs</a>.


### -field PaletteEntries

Number of palette entries. The value must be between 0 and 256.


### -field Palette

Array of <a href="https://msdn.microsoft.com/72e45756-b1aa-4db0-a6e7-2e6ea97211b4">MFPaletteEntry Union</a>s that contains the color table for a palettized format. The size of the array is given in the <b>PaletteEntries</b> member. If the format is not palettized, set <b>PaletteEntries</b> to zero.


## -see-also




<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

