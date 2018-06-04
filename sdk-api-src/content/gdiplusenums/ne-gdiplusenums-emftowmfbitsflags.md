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

# EmfToWmfBitsFlags enumeration


## -description


Specifies options for the <a href="https://msdn.microsoft.com/e3846642-b7cb-4191-98a3-622e3f0bdf69">Metafile::EmfToWmfBits</a> method, which converts an Enhanced Metafile (EMF) metafile to a Windows Metafile Format (WMF) metafile.


## -enum-fields




### -field EmfToWmfBitsFlagsDefault

Specifies the default conversion.


### -field EmfToWmfBitsFlagsEmbedEmf

Specifies that the source EMF metafile is embedded as a comment in the resulting WMF metafile.


### -field EmfToWmfBitsFlagsIncludePlaceable

Specifies that the resulting WMF metafile is in the placeable metafile format; that is, it has the additional 22-byte header required by a placeable metafile.


### -field EmfToWmfBitsFlagsNoXORClip

Specifies that the clipping region is stored in the metafile in the traditional way. If you do not set this flag, the <a href="https://msdn.microsoft.com/e3846642-b7cb-4191-98a3-622e3f0bdf69">Metafile::EmfToWmfBits</a> method applies an optimization that stores the clipping region as a path and simulates clipping by using the XOR operator.


## -see-also




<a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a>



<a href="https://msdn.microsoft.com/e3846642-b7cb-4191-98a3-622e3f0bdf69">Metafile::EmfToWmfBits</a>
 

 

