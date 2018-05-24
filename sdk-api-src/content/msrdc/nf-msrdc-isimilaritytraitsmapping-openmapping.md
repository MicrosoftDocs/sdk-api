---
UID: NF:msrdc.ISimilarityTraitsMapping.OpenMapping
title: ISimilarityTraitsMapping::OpenMapping
author: windows-driver-content
description: Opens the file mapping object for a similarity traits table file.
old-location: rdc\isimilaritytraitsmapping_openmapping.htm
old-project: Rdc
ms.assetid: 278d7b78-28c6-41ee-9060-5f7d757ef494
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ISimilarityTraitsMapping interface [Remote Differential Compression],OpenMapping method, ISimilarityTraitsMapping.OpenMapping, ISimilarityTraitsMapping::OpenMapping, OpenMapping, OpenMapping method [Remote Differential Compression], OpenMapping method [Remote Differential Compression],ISimilarityTraitsMapping interface, fs.isimilaritytraitsmapping_openmapping, msrdc/ISimilarityTraitsMapping::OpenMapping, rdc.isimilaritytraitsmapping_openmapping
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msrdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsRdc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RdcMappingAccessMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MsRdc.dll
api_name:
-	ISimilarityTraitsMapping.OpenMapping
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISimilarityTraitsMapping::OpenMapping


## -description


Opens the file mapping object for a similarity traits table file.


## -parameters




### -param accessMode [in]


<a href="https://msdn.microsoft.com/570fe290-1209-4bae-a56c-f6f663e53f87">RdcMappingAccessMode</a> enumeration value that specifies the desired access to the file mapping object.


### -param begin [in]

File offset, in bytes, where the file mapping is to begin.


### -param end [in]

File offset, in bytes, where the file mapping is to end.


### -param actualEnd [out]

Pointer to a location that receives the file offset, in bytes, of the actual end of the file mapping, rounded up to the nearest block size.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1ddc599b-5a9b-4807-9005-00793f9a6ed4">ISimilarityTraitsMapping</a>
 

 

