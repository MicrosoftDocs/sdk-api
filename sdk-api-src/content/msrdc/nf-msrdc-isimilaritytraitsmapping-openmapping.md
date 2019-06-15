---
UID: NF:msrdc.ISimilarityTraitsMapping.OpenMapping
title: ISimilarityTraitsMapping::OpenMapping (msrdc.h)
author: windows-sdk-content
description: Opens the file mapping object for a similarity traits table file.
old-location: rdc\isimilaritytraitsmapping_openmapping.htm
tech.root: rdc
ms.assetid: 278d7b78-28c6-41ee-9060-5f7d757ef494
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISimilarityTraitsMapping interface [Remote Differential Compression],OpenMapping method, ISimilarityTraitsMapping.OpenMapping, ISimilarityTraitsMapping::OpenMapping, OpenMapping, OpenMapping method [Remote Differential Compression], OpenMapping method [Remote Differential Compression],ISimilarityTraitsMapping interface, fs.isimilaritytraitsmapping_openmapping, msrdc/ISimilarityTraitsMapping::OpenMapping, rdc.isimilaritytraitsmapping_openmapping
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
 - ISimilarityTraitsMapping.OpenMapping
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISimilarityTraitsMapping::OpenMapping


## -description


Opens the file mapping object for a similarity traits table file.


## -parameters




### -param accessMode [in]


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/ne-msrdc-__midl___midl_itf_msrdc_0000_0000_0010">RdcMappingAccessMode</a> enumeration value that specifies the desired access to the file mapping object.


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
 

 

