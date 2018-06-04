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

# ENHMETAHEADER3 structure


## -description


The <b>ENHMETAHEADER3</b> structure contains enhanced-metafile data including the dimensions of the metafile image, the number of records in the metafile, and the resolution of the device on which the metafile was created.


## -struct-fields




### -field iType

Type: <b>DWORD</b>

Record type. Value is always EMR_HEADER. 


### -field nSize

Type: <b>DWORD</b>

Structure size, in bytes. This may be greater than the value returned by <b>sizeof</b>(<b>ENHMETAHEADER3</b>). 


### -field rclBounds

Type: <b>RECTL</b>

Bounding rectangle, in device units, for the image stored in the metafile. 


### -field rclFrame

Type: <b>RECTL</b>

Rectangle, in 0.01 millimeter units, that surrounds the image stored in the metafile. 


### -field dSignature

Type: <b>DWORD</b>

Must be ENHMETA_SIGNATURE. 


### -field nVersion

Type: <b>DWORD</b>

Version number of the metafile format. The current version is 0x10000. 


### -field nBytes

Type: <b>DWORD</b>

Size, in bytes, of the metafile. 


### -field nRecords

Type: <b>DWORD</b>

Number of records in the metafile.


### -field nHandles

Type: <b>WORD</b>

Number of handles in the metafile handle table. Handle index zero is reserved.


### -field sReserved

Type: <b>WORD</b>

Reserved. Must be zero. 


### -field nDescription

Type: <b>DWORD</b>

Number of characters in the string that contains the description of the metafile's contents. This member is 0 if the metafile does not have a description string.


### -field offDescription

Type: <b>DWORD</b>

Offset from the beginning of the <b>ENHMETAHEADER3</b> structure to the string that contains the description of the metafile's contents. This member is 0 if the metafile does not have a description string. 


### -field nPalEntries

Type: <b>DWORD</b>

Number of entries in the metafile palette.


### -field szlDevice

Type: <b>SIZEL</b>

Resolution, in pixels, of the reference device. 


### -field szlMillimeters

Type: <b>SIZEL</b>

Resolution, in millimeters, of the reference device. 

