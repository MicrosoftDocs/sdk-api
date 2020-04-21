---
UID: NF:msrdc.ISimilarityTraitsMapping.ResizeMapping
title: ISimilarityTraitsMapping::ResizeMapping (msrdc.h)
description: Resizes the file mapping object for a similarity traits table file.helpviewer_keywords: ["ISimilarityTraitsMapping interface [Remote Differential Compression]","ResizeMapping method","ISimilarityTraitsMapping.ResizeMapping","ISimilarityTraitsMapping::ResizeMapping","ResizeMapping","ResizeMapping method [Remote Differential Compression]","ResizeMapping method [Remote Differential Compression]","ISimilarityTraitsMapping interface","fs.isimilaritytraitsmapping_resizemapping","msrdc/ISimilarityTraitsMapping::ResizeMapping","rdc.isimilaritytraitsmapping_resizemapping"]
old-location: rdc\isimilaritytraitsmapping_resizemapping.htm
tech.root: rdc
ms.assetid: ea4fe3f9-7422-4673-90e4-4907fb8dd690
ms.date: 12/05/2018
ms.keywords: ISimilarityTraitsMapping interface [Remote Differential Compression],ResizeMapping method, ISimilarityTraitsMapping.ResizeMapping, ISimilarityTraitsMapping::ResizeMapping, ResizeMapping, ResizeMapping method [Remote Differential Compression], ResizeMapping method [Remote Differential Compression],ISimilarityTraitsMapping interface, fs.isimilaritytraitsmapping_resizemapping, msrdc/ISimilarityTraitsMapping::ResizeMapping, rdc.isimilaritytraitsmapping_resizemapping
f1_keywords:
- msrdc/ISimilarityTraitsMapping.ResizeMapping
dev_langs:
- c++
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
req.lib: 
req.dll: MsRdc.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- MsRdc.dll
api_name:
- ISimilarityTraitsMapping.ResizeMapping
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISimilarityTraitsMapping::ResizeMapping


## -description


Resizes the file mapping object for a similarity traits table file.


## -parameters




### -param accessMode [in]


<a href="https://docs.microsoft.com/windows/win32/api/msrdc/ne-msrdc-rdcmappingaccessmode">RdcMappingAccessMode</a> enumeration value that specifies the desired access to the file mapping object.


### -param begin [in]

File offset, in bytes, where the file mapping is to begin.


### -param end [in]

File offset, in bytes, where the file mapping is to end.


### -param actualEnd [out]

Pointer to a location that receives the file offset, in bytes, of the actual end of the file mapping, rounded up to the nearest block size.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytraitsmapping">ISimilarityTraitsMapping</a>
 

 

